# parser_bot.py
``` bash
pip install telethon
```
## Setup
1. **Telegram API Credentials:**
    - Obtain your `api_id` and `api_hash` from the [Telegram API Dashboard]().
    - Replace placeholders in the script:
``` python
     api_id = 'your_api_id'
     api_hash = 'your_api_hash'
```
1. **Group Details:**
    - Replace the group IDs in `malaysia_groups` and `vietnam_groups` with the actual IDs of Telegram groups you want to monitor.
    - Add corresponding links in the `group_links` dictionary for easy reference.

2. **Destination Chats:**
    - Replace `malaysia_chat` and `vietnam_chat` with the chat IDs where you want to forward alerts.

3. **Keywords:**
    - Customize the `keywords` list with the specific terms you want to monitor.

## Usage
1. **Run the Bot:**
    - Start the bot by executing the script:
``` bash
     python script_name.py
```
- The bot will log into your Telegram account (you'll need to verify the login via the Telegram app on your phone) and begin monitoring.

1. **What Happens:**
    - When the bot detects a message containing any of the specified keywords:
        - It sends a notification to the appropriate alert chat.
        - It forwards the original message for review.

2. **Stop the Bot:**
    - To stop the bot, use `Ctrl+C` or manually interrupt the execution.

## Example Configuration
``` python
api_id = '123456'
api_hash = 'abcdef1234567890'

malaysia_groups = ['group_id_1', 'group_id_2']
vietnam_groups = ['group_id_3', 'group_id_4']

malaysia_chat = 'your_malaysia_alert_chat_id'
vietnam_chat = 'your_vietnam_alert_chat_id'

keywords = ['keyword1', 'keyword2', 'keyword3']
```
## Notes
- Log files can be useful for tracking bot activity and diagnosing issues (logged via `logging`).
- Ensure your Telegram credentials and group/chat IDs are kept private and not exposed in public repositories.

## Potential Improvements
1. **Dynamic Group Management:**
    - Add a feature to dynamically manage monitored groups via a configuration file or a bot command.

2. **Extended Keyword Handling:**
    - Allow regex patterns for more advanced keyword matching.

3. **Error Handling:**
    - Add better error-handling mechanisms to ensure the bot continues running even after encountering exceptions.

## License
This project is licensed under the MIT License. You are free to modify, share, and use it as needed.

