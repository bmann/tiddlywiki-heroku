# TiddlyWiki on Heroku

TiddlyWiki setup to run well on Heroku.

Runs TiddlyWiki 5.1.18 or higher, using the built in web server.

The `package.json` file uses the start script to control options to the [listen command](https://tiddlywiki.com/static/ListenCommand.html), which can be set in the Heroku environment variables. Read the [full listen of web server command parameters](https://tiddlywiki.com/static/WebServer.html).

* host: set to `0.0.0.0` to bind to Heroku's system
* port: set to `$PORT` as supplied by Heroku
* readers: allows anonymous readers; set to `$ADMIN` for private wikis
* writers: any authenticated user can write
* username: set from `$ADMIN`
* password: set from `$PASSWORD`

## Plugins

* TiddlyMap
* Markdown

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)