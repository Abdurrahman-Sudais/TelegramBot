# TelegramBot

A Python-based Telegram bot for managing groups, providing moderation tools, and tracking group statistics.

## ✨ Features

- **Group Management**: Commands for locking and unlocking the group.
- **User Moderation**: Commands to mute, unmute, ban, and kick users.
- **Activity Tracking**: Uses SQLite to record member message counts and daily active users.
- **Group Statistics**: Provides a `/stats` command summarizing group activity, member counts, and admin presence.
- **Role-Based Access**: Restricts moderation commands to group administrators.

## 🛠️ Tech Stack

- **Python 3**
- `python-telegram-bot` (Telegram API wrapper)
- `sqlite3` (Local database for statistics)
- **Railway** (Configuration provided via `railway.toml`)

## 📁 Project Structure

```text
TelegramBot/
├── bot.py               # Main bot logic and SQLite configuration
├── Dockerfile           # Docker container configuration
├── railway.toml         # Railway deployment config
├── requirements.txt     # Python dependencies
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- A Telegram Bot token (from [BotFather](https://core.telegram.org/bots#botfather))

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Abdurrahman-Sudais/TelegramBot.git
   cd TelegramBot
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## ⚙️ Configuration

The bot relies on environment variables for security. You must export your bot token before running the script:

**Linux / macOS:**
```bash
export BOT_TOKEN=your_telegram_bot_token_here
```

**Windows (Command Prompt):**
```cmd
set BOT_TOKEN=your_telegram_bot_token_here
```

## ▶️ Usage

Start the bot locally:
```bash
python bot.py
```

### Available Commands

- `/start` - Check if the bot is active
- `/help` - View the list of available commands
- `/stats` - Display member and message statistics for the current day

**Admin Only Commands:**
- `/lock` - Prevent standard members from sending messages
- `/unlock` - Allow standard members to send messages
- `/mute @username` - Temporarily disable a user's messaging permissions (or reply to a message)
- `/unmute @username` - Restore a user's messaging permissions
- `/ban @username` - Remove and ban a user from the group
- `/kick @username` - Remove a user from the group (allows them to rejoin later)

## 🌐 Deployment

This bot is configured for easy deployment on [Railway](https://railway.app/). Ensure you configure the `BOT_TOKEN` environment variable in your Railway project settings. The provided `Dockerfile` and `railway.toml` handle the build and execution process automatically.

## 👨🏽‍💻 Author

**Abdurrahman Sudais**

- GitHub: [https://github.com/Abdurrahman-Sudais](https://github.com/Abdurrahman-Sudais)
- Portfolio: [https://call-him-sudais.vercel.app](https://call-him-sudais.vercel.app)
