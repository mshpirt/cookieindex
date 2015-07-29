# Cookie-based MongoDB Session Storage
app that creates and stores express sessions with mongostore 

The routes for this app  are:

1) Index (New Game) > Start > Newgame > Load > Game

2) Index (Load Game) > Load > Game

To run this app, install node.js, express.js through npm, and mongodb. Homebrew recommended for OSX.

Get a mongo instance running at 127.0.0.1:27017 (default). If it spits an error do sudo mkdir -p /data/db.

Run npm update after cloning the repo locally to download/update all the dependencies. Then npm start or nodemon ./bin/www if you have that installed.

This program creates a session in the login db of mongo in the users collection upon a user's first visit. In a New Game, the users enters a name and this is paired with their session ID for a database entry in the users database in the users collection. Upon loading the game, the user's name is displayed on the page.

In the user creation route, any new user created overwrites the previous user. Thus, you have a persistent cookie-based save file and can reset the name you assign yourself.

Tested on Ubuntu and OSX.