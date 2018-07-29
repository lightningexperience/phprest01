# php-api
<a href="https://heroku.com/deploy">
  <img src="https://www.herokucdn.com/deploy/button.svg" alt="Deploy">
</a>


What this does: This app would connect to a Salesforce Org and then select, update, delete accounts.

Caution: Use this only in a free DE Org you have spun off for demo/test. This app is not tested for production.

Configurations:

Fork this repo.

Press the Deploy button. The The deploy button is created by putting in the following lines of code in this readme:
<a href="https://heroku.com/deploy"><img src="https://www.herokucdn.com/deploy/button.svg" alt="Deploy"></a>
To read more about other options in Deploy Button: https://devcenter.heroku.com/articles/heroku-button

Choose an app name.

When the app deploys then go to "Manage App" and link your own GitHub repo (that is a fork of this) and choose Automatic Deploys.

In the following configurations, replace phprest001 with the app name you have chosen above.


In a Salesforce Org of your choice - create a Remote Site entry (https://phprest001.herokuapp.com/).

Create a Connected App - select the checkbox "Enable OuAuth settings" - put the Callback URL as https://phprest001.herokuapp.com/oauth_callback.php and choose everything as "Selected oAuth Scopes". Copy the secret ID and key and update the config.php with those values. The REDIRECT_URI in config.php is  "https://phprest001.herokuapp.com/oauth_callback.php Though we store the config values in source code, ideally, an app’s environment-specific configuration should be stored in environment variables (not in the app’s source code): https://devcenter.heroku.com/articles/config-vars

