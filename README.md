[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

# Bürgerämter Termin

Leverages the [termin_de](https://github.com/Strech/termin_de) tool to provide automatic monitoring of available Bürgeramt slots directly on the cloud, ready to deploy on Heroku. Use with moderation and remember to shut it off afterwards.

## Settings

Set your email address:

    $ heroku config:set EMAIL_TO=john.doe@example.com

Set the before date parameter:

    $ heroku config:set BEFORE_DATE=2016-01-30

## License

This code is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
