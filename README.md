# discord2sheet-bot

This bot allows users to submit messages directly to your Google Sheet.

Example:

`!s Hello world, How are you today?`

Output:

Username - UserID - Date - Field 1 - Field 2

![Google Sheet](https://i.imgur.com/MFx25Ik.png)

## How to set it up

**Step 1:** Enable the API and download credentials.json. This can be done here: https://developers.google.com/sheets/api/quickstart/python#step_1_turn_on_the

Make sure credentials.json is stored in the same directory as the bot.

**Step 2:** Open init.py and change the following values(<>):

SPREADSHEET_ID = <> - The ID of the spreashsheet to store the data. It can be found on the URL once opened.

FIELDS = <> - Amount of fields/cells that get stored. They are on the user's message seperated by comma (!s field1, field2,field 3)

client.run('<>') - The token of the Discord bot.

**Step 3:** Install Python dependencies

If you haven't installed Python yet, download it [here](https://www.python.org/).

Install discordpy: `pip install discord.py`

Run the pip command listed here: https://developers.google.com/sheets/api/quickstart/python#step_2_install_the_google_client_library

**Step 4:** Run the bot

`python init.py`

------

## Additional configutations

REQUIREDROLE = <> - If you want to restrict the command to a specific role, insert here the role id. If not, insert `None`.

RANGE_NAME = <> - Where the data should go in the spreadsheet. Default value is `A1`.

DATA = <> - What data goes to the rows, seperated by `[]`. Example: `DATA = [result[0]] + [''] + [result[1]]`
