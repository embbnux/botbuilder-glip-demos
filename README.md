# botbuilder-glip-demos

[![NPM Version](https://img.shields.io/npm/v/botbuilder-glip.svg?style=flat-square)](https://www.npmjs.com/package/botbuilder-glip)

RingCentral Glip with botbuilder demos

## Prerequisites

* Node.js > 8
* [Ngrok](https://ngrok.com/) to create a secure tunnel to local host
* [RingCentral developer free account](https://developer.ringcentral.com) to create a new app with platform type -"Server/bot"
* Microsoft LUIS account (optional)

## How to demo

### Clone this repo

```
$ git clone https://github.com/embbnux/botbuilder-glip-demos.git
$ cd botbuilder-glip-demos
$ yarn install
```

### Start Ngrok

```
$ ngrok http 3978
```
And you will get a ngrok domain, such as `https://981c576d.ngrok.io`. Use this as glip bot server url.

### Create `.env` file in project root folder

```
GLIP_API_SERVER=https://platform.devtest.ringcentral.com
GLIP_CLIENT_ID=YOUR_RINGCENTRAL_BOT_APP_ID
GLIP_CLIENT_SECRET=YOUR_RINGCENTRAL_BOT_APP_SECRET
GLIP_BOT_SERVER=YOUR_GLIP_BOT_SERVER
GLIP_BOT_VERIFICATION_TOKEN=YOUR_GLIP_BOT_VERIFICATION
LUIS_MODEL_URL=YOUR_LUIS_MODEL_URL
```

### Start demo

```
$ node index.js
```

Add bot to your glip with `Add to Glip` button in your bot page.

### Play with LUIS

You need to create a app in LUIS with some intents. And publish your LUIS, and set LUIS model url in `.env` file

```
$ node bot_with_luis.js
```
