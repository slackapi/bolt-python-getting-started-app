# Getting Started ⚡️ Bolt for Python

> Slack app example from 📚 [Getting started with Bolt for Python](https://docs.slack.dev/tools/bolt-python/getting-started)

## Overview

This is a Slack app built with the [Bolt for Python framework](https://docs.slack.dev/tools/bolt-python/) that showcases responding to events and interactive buttons.

## Running locally

### Using Slack CLI

Install the latest version of the Slack CLI for your operating system:

- [Slack CLI for macOS & Linux](https://docs.slack.dev/tools/slack-cli/guides/installing-the-slack-cli-for-mac-and-linux/)
- [Slack CLI for Windows](https://docs.slack.dev/tools/slack-cli/guides/installing-the-slack-cli-for-windows/)

You'll also need to log in if this is your first time using the Slack CLI.

```sh
slack login
```

#### Initializing the project

```sh
slack create bolt-python-getting-started --template slack-samples/bolt-python-getting-started-app
cd bolt-python-getting-started
```

#### Running the app

```sh
slack run
```

<details>
<summary><h3>Using Terminal</h3></summary>

#### 1. Setup environment variables

```zsh
# Replace with your tokens
export SLACK_BOT_TOKEN=<your-bot-token>
export SLACK_APP_TOKEN=<your-app-level-token>
```

#### 2. Setup your local project

```zsh
# Clone this project onto your machine
git clone https://github.com/slack-samples/bolt-python-getting-started-app.git

# Change into this project
cd bolt-python-getting-started-app/

# Setup virtual environment
python3 -m venv .venv
source .venv/bin/activate

# Install the dependencies
pip install -r requirements.txt
```

#### 3. Start servers

```zsh
python3 app.py
```

</details>

## More examples

Looking for more examples of Bolt for Python? Browse to [bolt-python/examples/](https://github.com/slackapi/bolt-python/tree/main/examples) for a long list of usage, server, and deployment code samples!

## Contributing

### Issues and questions

Found a bug or have a question about this project? We'd love to hear from you!

1. Browse to [slackapi/bolt-python/issues](https://github.com/slackapi/bolt-python/issues/new/choose)
1. Create a new issue
1. Mention that you're using this example app

See you there and thanks for helping to improve Bolt for everyone!
