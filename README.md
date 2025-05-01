# Age Calculator Slack Bot

A simple Slack bot that calculates a user's age based on their year of birth. Built with Go and the Slacker library.

## Features

- Responds to commands in Slack
- Calculates age based on birth year
- Displays command event details for monitoring

## Prerequisites

- Go installed on your machine
- Slack workspace with permissions to add apps
- Slack Bot Token and App Token

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/age-slack-bot.git
   cd age-slack-bot
   ```

2. Install dependencies:
   ```bash
   go mod download
   ```

3. Set up environment variables:
   ```bash
   export SLACK_BOT_TOKEN="your-bot-token"
   export SLACK_APP_TOKEN="your-app-token"
   ```

## Slack App Setup

1. Go to [Slack API](https://api.slack.com/apps) and create a new app
2. Enable Socket Mode
3. Add the following Bot Token Scopes:
   - `app_mentions:read`
   - `chat:write`
   - `commands`
4. Install the app to your workspace
5. Save the Bot Token and App Token for environment variables

## Usage

1. Run the bot:
   ```bash
   go run main.go
   ```

2. In your Slack workspace, use the command:
   ```
   my yob is <year>
   ```
   For example: `my yob is 1990`

3. The bot will respond with your calculated age.

## How It Works

The bot calculates age by subtracting the provided birth year from 2025. For example, if you were born in 1990, your age would be calculated as 2025 - 1990 = 35.

## Dependencies

- [github.com/shomali11/slacker](https://github.com/shomali11/slacker) - Framework for creating Slack bots

## License

[Include your license information here]

## Contributing

Contributions, issues, and feature requests are welcome!