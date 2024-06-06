Certainly! Below is a complete README with the appropriate repository commands included:

---

# Discord Status Rotator README

## Introduction
The Discord Status Rotator is a Python script designed to automatically rotate and update your custom status message on Discord. It reads status messages from a file, updates your Discord status at regular intervals, and optionally clears the console periodically. This script uses the Discord API for updating statuses and requires a valid Discord token.

## Features
- Rotates through a list of status messages.
- Updates the Discord custom status and activity status.
- Periodically clears the console for better readability.
- Color-coded console output for easy status monitoring.

## Requirements
- Python 3.6+
- `requests` library
- `colorama` library

## Installation

1. **Clone the Repository**:
   ```sh
   git clone https://github.com/whosdior/statuschanger.git
   cd statuschanger
   ```

2. **Install Dependencies**:
   ```sh
   pip install requests colorama
   ```

3. **Create Configuration Files**:
   - `config.json`: Store your configuration settings.
   - `text.txt`: List of statuses to rotate through.

## Configuration

### `config.json`
Create a `config.json` file in the same directory as the script with the following structure:

```json
{
  "token": "YOUR_DISCORD_TOKEN",
  "clear_enabled": true,
  "clear_interval": 10,
  "speed_rotator": 5,
  "status_sequence": ["online", "idle", "dnd", "invisible"]
}
```

### `text.txt`
Create a `text.txt` file with one status message per line:

```
Playing a game
Coding in Python
Watching a movie
Listening to music
```

## Usage

1. **Run the Script**:
   ```sh
   python status.py
   ```

## Code Overview

### Libraries and Modules
- `requests`: For making HTTP requests to the Discord API.
- `time`: For handling time-based operations.
- `json`: For loading configuration files.
- `os`: For clearing the console.
- `colorama`: For colorizing console output.

### Functions
- `read_statuses(file_name)`: Reads status messages from a file.
- `get_user_info(token)`: Retrieves the username associated with the provided Discord token.
- `change_status(token, message, status)`: Updates the Discord custom status.
- `clear_console()`: Clears the console.
- `load_config()`: Loads configuration settings from a JSON file.
- `color_text(text, color_code)`: Colorizes text for console output.

### Main Script
- Loads the configuration and status messages.
- Enters an infinite loop to rotate and update the status messages at specified intervals.
- Periodically clears the console if configured to do so.

## Conclusion
The Discord Status Rotator is a simple yet effective tool for managing your Discord custom status messages automatically. With configurable settings and easy-to-use file-based input, it offers flexibility and convenience for keeping your status messages fresh and up-to-date. Customize the `config.json` and `text.txt` files to suit your preferences and enjoy automated status rotation on Discord.
