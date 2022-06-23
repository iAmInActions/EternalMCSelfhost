# Customisation
___

This page Explains how you can customise your install to fit your needs. Currently there are four supported options: Changing the target server (In case you dont actually want to play on EternalMC), Changing the default ports, setting a custom texture pack and changing the experimental options.

___

## Changing the forwarded server

To change which Minecraft: Java Edition* server gets forwarded to the client, edit eagler.js in an UTF-8 compliant text editor (leafpad or nano work well; for you windows folks try Notepad++) and edit the lines containing the following variables:
```
const mcHost = "ip-of-minecraft.server";
const mcPort = 25565; // 25565 is the default for all minecraft servers. If your server is running on a different port, you need to change it to that port.
const serverName = "ServerName";
const serverMotd = ["Motd Line 1", "Motd Line 2"];
const serverMaxPlayers = 25; // Max players allowed
const serverOnlinePlayers = 3; // How many players are shown (useful for using the Player list as a sort of README file
const serverPlayers = ["notaplayer1", "notaplayer2", "notaplayer3"]; // Player list
const serverIcon = "icon.png"; // set to null for no icon. MUST be 64x64. can be a url, if you want.
```

*Only 1.5.2 in offline mode is supported. Most cracked servers with ProtocolSupport will work. Please note that depending on the servers distance and location performance may suffer when connecting over a proxy.

## Changing the default ports

To change the ports that your server will be running on, edit eagler.js in an UTF-8 compliant text editor (leafpad or nano work well; for you windows folks try Notepad++) and edit the lines containing the following variables:
```
const listenPort = 25565; // The port of the vanilla proxy in case you want to be able to use ayuncrafts internal proxy as a bounce server
[...]
const httpPort = 8088; // The port you enter in your web browser (http://domain.top:port/)
```

## Changing the texture pack

To change the texture pack you will need to firstly make it Eaglercraft compatible. (Tutorial: https://youtu.be/lGctod13pyU)

Then you simply place the freshly created assets.epk into the www folder. You can either rename or overwrite old one.

## Experimental options

The file eagler.js containst a few experimental options. These should be left as is in a production environment but depending on your use case you might need to change them. Below is a list of options and what they do.
```
const timeout = 10000; // Change the timeout for the proxy. Value in milliseconds
const changeProtocol = true; // Wether or not the proxy should change the version bit of the Minecraft protocol to support eaglercraft. If your server is not a vanilla server and you are having issues connecting you might have to disable it.
const removeSkin = true; // Should the server remove skin data or not? Usually set to true to reduce lag and compatibility issues. Disabling it will let you use skins using a plugin but it will also increase the ping.
const prefix = "www"; // The directory that the Client is stored in. If you have multiple clients you can change this to select the active one. Default is www.
```
