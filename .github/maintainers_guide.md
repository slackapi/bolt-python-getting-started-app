# Maintainers Guide

This document describes tools, tasks and workflow that one needs to be familiar with in order to effectively maintain
this project. If you use this repository within your own software as is but don't plan on modifying it, this guide is
**not** for you.

## Tools

### Python (and friends)

We recommend using [pyenv](https://github.com/pyenv/pyenv) for Python runtime management. If you use macOS, follow the following steps:

```bash
$ brew update
$ brew install pyenv
```

Install necessary Python runtimes for development/testing. You can rely on Travis CI builds for testing with various major versions. https://github.com/slackapi/bolt-python/blob/main/.travis.yml

```bash
$ pyenv install -l | grep -v "-e[conda|stackless|pypy]"

$ pyenv install 3.8.5 # select the latest patch version
$ pyenv local 3.8.5

$ pyenv versions
  system
  3.6.10
  3.7.7
* 3.8.5 (set by /path-to-bolt-python/.python-version)

$ pyenv rehash
```

Then, you can create a new Virtual Environment this way:

```
$ python -m venv .venv
$ source .venv/bin/activate
```

## Tasks

### Updating

This package is a dependency for our guides and other example apps. There are many ways to configure a sample app. We prefer to keep a single version of `app.js` which should be consistent with the instructions and code blocks on the [Bolt JS Getting Started guide](https://slack.dev/bolt-js/tutorial/getting-started). This reduces the possibility of drift ocurring between multiple versions. 

When making changes to this repo, it's also important to keep all of our other guides and apps up-to-date.

- Guides found at [slackapi/bolt-python/docs/](https://github.com/slackapi/bolt-python/tree/main/docs)
- Example apps at [slackapi/bolt-python/examples/](https://github.com/slackapi/bolt-python/tree/main/examples)

### Testing

This repository does not have unit tests.

### Releasing

1.  Create the commit for the release:
    *  Update any dependency versions 
    *  Update `version.py` with the new version number. For example `2.2.0`.
    *  Commit with a message including the new version number. For example `v2.2.0`.
    *  Tag the commit with the version number. For example `git tag 2.2.0`.

2.  Merge into main repository
    *  Create a pull request with the commit that was just made. Be certain to include the tag. For
       example: `git push username main:rel-v1.0.8 && git push --tags username`.
    *  Once tests pass and a reviewer has approved, merge the pull request. You will also want to
       update your local `main` branch.
    *  Push the new tag up to origin `git push --tags origin`.

3.  Distribute the release
    *  At the moment this repository is not distributed on pypi.
    *  It is only downloaded or cloned from GitHub.

4.  Announce on community.slack.com in #slack-api and #tools-bolt

## Workflow

### Versioning and Tags

This project uses semantic versioning, expressed through the numbering scheme of
[PEP-0440](https://www.python.org/dev/peps/pep-0440/).

### Fork

As a maintainer, the development you do will be almost entirely off of your forked version of this repository. The exception to this rule pertains to multiple collaborators working on the same feature, which is detailed in the **Branches** section below.

### Branches

`main` is where active development occurs. Long running named feature branches are occasionally created for
collaboration on a feature that has a large scope (because everyone cannot push commits to another person's open Pull
Request). At some point in the future after a major version increment, there may be maintenance branches for older major
versions.

### Issue Management

All issues are managed under https://github.com/slackapi/bolt-python/issues.

Use the label `area:examples` to organize issues related to this example app repository.

## Everything else

When in doubt, find the other maintainers and ask.