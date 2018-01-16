# rcon-discord
Ein kleiner Bot für den großen Noah.

# Features

This bot adds to commands to your discord server.

- `/adduser <name>` to allow users to whitelist themselves on your minecraft server.
    - Via config you can restrict this feature to admin users
- `/removeuser <name>` to allow admins to remove users from the whitelist.

# How to install.
## Rcon

- Go to your `server.properties` and set `enable-rcon=true`
- Restart your Server. Now there are two additional config parameters in `server.properties`
- Set `rcon.port` to any number between `1000` to `65535`. `25575` is the recommended number.
- Set `rcon.password` to any password you like. The more complicated the better.
- Whatever you set to those two values you have the same in your `config.json` for the discord bot.

## This bot
- Head to over to [Release][1] and Download the latest `.jar` file
- In the directory you want to run the bot. Create a `config.json` with the following content: 

```json
{
  "rcon": {
    "server": "YOUR MINECRAFT SERVER",
    "port": 25575 /*or whatever rcon port you are using. look into your server.properties */,
    "password": "RCON-PASSWORD" /* yet again -> server.properties */
  },
  "selfinvite": true, /* Whether user can use this or only admins. */
  "discord": {
    "admins": [
      "YOUR DISCORD USER ID. Find out using Developer mode.",
      "A SECOND ID"
    ],
    "token": "Your bots token. Create one over at https://discordapp.com/developers/applications/me"
  }
}
```
-  After that run the jar using double click or `java -jar <filename.jar>`


[1]: https://github.com/romangraef/rcon-discord/releases
