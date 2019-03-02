# league-notify-config
Config for league-notify-api and league-notify-web. Uses [config-leaf](https://github.com/jed/config-leaf) to encrypt/decrypt to the CAST5 cipher.

## Table of content

* [Installation](#installation)
* [Configuration](#configuration)

## Installation
To use the config, it needs to be decrypted. To do this, run:

    npm run decrypt

It will then prompt you to enter the password that it was encrypted with. Do this and you will end up with a decrypted `config.js` file that you can use in the `league-notify` apps.

## Configuration
The configuration is a `js` file that looks like the following:

```js
const config = {
    app: {
        port: YOUR_PORT_NUMBER
    },
    db: {
        host: YOUR_DB_HOST,
        port: YOUR_DB_PORT,
        name: YOUR_DB_NAME
    }
};

module.exports = config;
```

## Usage
To use the decrypted config, simply include it as follows:

```js
    const config = require('PATH_TO_YOUR_CONFIG/config');
```

You can then use it as a regular Javascript object.