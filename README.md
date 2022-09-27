
# Egg, Inc. Python API

This was made to be a stupidly simple way to interact with the API for Auxbrain's game: Egg, Inc.

The only thing you need to add to python is the Requests package, this can be done by running `pip install requests`

Over on [repl.it](https://replit.com/@thenicopanda1/MadPinkUpgrade#main.py) I have a working demo of this project.

## Current Options
* `get_first_contact(ei_user_id)` : Used to pull the vast majority of data, including but certainly not limited to: Soul Eggs, Golden Eggs, Your Artifacts, Every Contract You've Done, etc.
* `get_periodicals(ei_user_id)` : Used to pull event information, primarily events such as 2x Prestige, or currently available Conracts.
* `get_config(ei_user_id)` : Used to pull all sorts of information, ranging from the URL to certain images, to the price of different boosts.
* `get_afx_config(ei_user_id)` : Used to pull information on Artifacts, from the URL to the images, to the xp needed to unlock a recipe.
* `get_daily_gift_info()` : Used to determine Current Day Number and Seconds Until Next Day.
* `get_coop_status(ei_user_id, contract_identifier, coop_identifier)` : Used to pull information on a specific coop, NOTE: Coop Name And Identifier Must Be Lowercase!

## Basics
* To start using this project add `ei.py`, `ei_pb2.py`, and the folder `google` to your folder. Then import the ei file into wherever you're workin, it should look something like ```from ei import *``` or maybe `from ei import get_first_contact`.
* Every Request will return as a Dictionary. [Here](https://www.w3schools.com/python/python_dictionaries.asp) is a quick refresher on Python Dictionaries if you feel you cannot interact with one.
* `ei_user_id` is just your EID from the game, this can be found by going to `Settings-> Privacy & Data-> and it's under the 2 red buttons.
* `contract_identifier` is the ID of the contract, for example: The contract `Depleted Reserves` has an ID  of `heat-wave-2022`. This ID can be found in `get_periodicals()`.
* `coop_identifier` is the Coop Code.
