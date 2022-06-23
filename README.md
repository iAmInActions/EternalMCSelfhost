# EternalMC Online Self-Host Package
___

This package provides a way to bypass domain blocking for the EternalMC Minecraft Server (and others; see CUSTOMISATION.md) by simply hosting it on your own server or PC. Software like cloudflare, portmap.io or ngrok may be used in conjunction with this.
___

## Installation

The setup is quite simple. You need to have a somewhat recent version of node.js and npm installed (yes, i know that node sucks but its only server side so no user has to deal with it) and ideally you would be running a modern Unix-like system like Linux, BSD or Mac OS X. Native Windows is not officially supported and all users installing this under Windows may not receive any support by me. It might still be possible to run under Windows natively though. For stability and security reasons I highly recommend using WSL or WSL2 under Windows as it provides a Linux environment.

Enough talking around though. Here are the steps to installation:
```
# Step 1: Cloning the repository
git clone https://github.com/iAmInActions/EternalMCSelfhost
cd EternalMCSelfhost
# Step 2: Installing dependencies
npm install
# Step 3: Running the proxy
./runme.sh
```
