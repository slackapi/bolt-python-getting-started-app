# Getting Started ⚡️ Bolt for Python
> Slack app example from 📚 [Getting started with Bolt for Python][1]

## Overview

This is a Slack app built with the [Bolt for Python framework][2] that showcases
responding to events and interactive buttons.

## Running locally

### 1. Setup environment variables

```zsh
# Replace with your signing secret and token
export SLACK_BOT_TOKEN=<your-bot-token>
export SLACK_SIGNING_SECRET=<your-signing-secret>
```

### 2. Setup your local project

```zsh
# Clone this project onto your machine
git clone https://github.com/slackapi/bolt-python-getting-started-app.git

# Change into this project
cd bolt-python-getting-started-app/

# Setup virtual environment
python3 -m venv .venv
source .venv/bin/activate

# Install the dependencies
pip install -r requirements.txt
```

### 3. Start servers

[Setup ngrok][3] to create a local requests URL for development.

```zsh
ngrok http 3000
python3 app.py
```

## More examples

Looking for more examples of Bolt for Python? Browse to [bolt-python/examples/][5] for a long list of usage, server, and deployment code samples!

## Contributing

### Issues and questions

Found a bug or have a question about this project? We'd love to hear from you!

1. Browse to [slackapi/bolt-python/issues][4]
1. Create a new issue
1. Mention that you're using this example app

See you there and thanks for helping to improve Bolt for everyone!

[1]: https://slack.dev/bolt-python/tutorial/getting-started
[2]: https://slack.dev/bolt-python/
[3]: https://slack.dev/bolt-python/tutorial/getting-started#setting-up-events
[4]: https://github.com/slackapi/bolt-python/issues/new/choose
[5]: https://github.com/slackapi/bolt-python/tree/main/examples