# Discord Bot Tutorial
## Setup
1. Create a folder in your file system and initialize an empty node project using `npm init`. You can type whatever you want as project names, description, etc.
2. Now you need to install the Discord.JS Framework in order to communicate with the discord servers by typing `npm install discord.js`.
3. Now go to [Discord Developers](https://discord.com/developers/applications), login and create your own Application.
4. After having created the application you select it and you see a Client ID (next to the bots image), which will be important soon.
5. Once that's done, select your newly created application and 'convert it' to a bot using the menu on the left (Menu Item: Bot)
6. Now you see a token right to the bot image. This will be important later on, so remember where to find it.
7. Now go on [Discord Permissions Calculator](https://discordapi.com/permissions.html) and select all the required permissions and enter the Client ID of your Discord Bot. (from step 4)
8. The link generated below can add the bot to any server, where you are the admin. Note: You can give this link to any person.
9. Add the bot to the server you want him to be active on.

## Coding Pt. 1
1. Create a file with the same name as the entry point you decided earlier on (you can look that up in package.json).
2. Add the following line, so we can use the previously installed framework in our code:
```js
const Discord = require('discord.js');
```
3. Now we need to create a Discord Client for our bot, which we'll do with the following line:
```js
const bot = new Discord.Client();
```
4. As soon as we have done that, we can create a very simple bot, by just logging the bot in, using following line: (Note: this should be the last line).
```js
bot.login('[placeholder for the token from the Discord Developers page]');
```
5. Since we don't want our bot just to join and be silent forever, we will implement a very simple logging mechanism, so we - the bot creators know, when the bot is starting. Insert this line above the `login` line.
```js
bot.on('ready', () => {
    console.log('Bot is now online!');
});
```
=> Now the bot gives us a message when he log's in.

## Starting Bot
To start the bot you simply go into the console (navigate to the folder) and start the bot using `node .`
