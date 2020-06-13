# Get tokens for Google Home Foyer API

## Intro
This script (python 3) generates tokens that can be used when making requests to the Google Home Foyer API.
There are 2 kinds of tokens used here:

1. Master token - Is in the form `aas_et/***` and is long lived. Needs Google username and password.
2. Access token - Is in the form `ya29.***` and lasts for an hour. Needs Master token to generate.

If you do not want to store the Google account password in plaintext,
get the master token once, and set it as an override value.

It's safer/easier to generate an app password and use it instead of the actual password.
It still has the same access as the regular password, but still better than using the real password while scripting.
(https://myaccount.google.com/apppasswords)

## Usage

```sh
# Install python requirements
pip install gpsoauth

# Update the constants at the beginning of the file

# Get the tokens!
python3 get_tokens.py
```