# xero-bank-extract-test

This cli example dumps out bank transactions from a Xero organization, I recommend
testing it with the Demo Company that is provided







This command line utility will attempt to auth to xero and export bank transactions.

If the access token is expired it will attempt to refresh the access token. If this
fails, the access token will nee

## Create a Xero App in developer centre

To obtain your API keys, follow these steps and create a Xero app

* Login to [Xero developer center](https://developer.xero.com/myapps)
* Click "New App" link
* Enter your App name ("xero-bank-extract-test"), company url etc
* Enter the redirect URI (your callback url - i.e. `http://localhost:5000/callback`)
* Agree to terms and condition and click "Create App".
* Click "Generate a secret" button.
* Copy your client id and client secret and save for use later.
* Click the "Save" button. You secret is now hidden.

## Configure API keys
* Edit `config.py` file in the root directory of this project & add the 2 variables
```python
CLIENT_ID = "...client id string..."
CLIENT_SECRET = "...client secret string..."
