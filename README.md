# Set a custom Discord RPC

This guide explains how to make a custom RPC status on Discord!

### Requirements
* You must be logged in to a Discord client in your desktop, so no mobile or web
* You need [Visual Studio Code](https://code.visualstudio.com/) or another code editor
* You need [NodeJS](https://nodejs.org/en/download/) (includes NPM, which is needed as well)

## Step One: Make the application
* Go to the [Developer Portal](https://discord.com/developers/applications) > New Application
* Give it the name you want your RPC status to have
* Under the tab Rich Presence > Art Assets, upload an image (if you want one) and note the name

## Step Two: Creating the project
* Make a new folder and open it in your code editor
* Open a terminal in your project's folder and initialize the project with `npm init -y` (if it gives an error run the interactive setup with `npm init`)
* Install the `discord-rpc` package: `npm install discord-rpc`
* Now, go to `config.json` file and change info to fit your DRP!
```js
{
    "clientId": "857315904253329431",
    "rich_presence": {
        "details": "If im using this status, im AFK",
        "state": "Got some time left dont I?",
        "assets": {
            "largeImageText": "Subscribe to my youtube lmao",
            "largeImageKey": "pink",
            "smallImageText": "Check out my website?",
            "smallImageKey": "large"
        },
        "buttons": {
            "primary": {
                "buttonLabelText": "YouTube",
                "buttonRedirectUrl": "http://YouTube.com/Zuxces"
            },
            "secondary": {
                "buttonLabelText": "Reddit",
                "buttonRedirectUrl": "https://zuxces.net/"
            }
        },
        "timestamps": {
            "startTimestamp": "91239173",
            "endTimestamp": "12317903",
            "useTimer": "true"
        }
    }
}

```

## Step Three: Running the RPC
* Save all files, then run `node index.js` in the terminal
* It should log that it's ready, and the RPC status should appear on your profile!

## Contact
* If you have any questions, you can comment on this gist
* If you want to contact me, you can join [Discord Server](https://dsc.gg/Zuxces) or [Programming Server](https://dsc.gg/Zuxces) 
