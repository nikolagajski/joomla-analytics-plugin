# Joomla analytics plugin
Joomla plugin for tracking and storing the tracking data in the 1st party Aesirx Analytics server.

This plugin is for the latest Joomla form 4.2.9 and newer.

First you will need to set up the 1st party Analytics server.
The instructions are here [AesirX 1st Party Server](https://github.com/aesirxio/analytics-1stparty).

After you set up the server you will install the Joomla plugin and in the configuration you will need to enter
the URL of the 1st party Aesirx Analytics server example [http://example.com:1000/] and publish the plugin.

And this is all set. 
The tracking from your Joomla site will be stored in the Mongo database on the 1st party server.

## For local setup
To install this you will need to clone this repo locally with command:

`git clone https://github.com/aesirxio/joomla-analytics-plugin.git`

## PHP set up

After that you can run the next commands.

`npm i` - initialize libraries

`npm run build` - for building Joomla zip installer (PHP 7.2 or higher)

`npm run watch` - for watching changes in the JS when developing

## Docker set up

### Linux

Alternatively can be used docker-compose with npm and php included, see available commands in `Makefile`:

`make init` - initialize libraries

`make build` - for building Joomla zip installer (PHP 7.2 or higher)

`make watch` - for watching changes in the JS when developing

### Windows

If you don't have Makefile set uo on Windows you can use direct docker commands.

`docker-compose run php-npm npm i` - initialize libraries

`docker-compose run php-npm npm run build` - for building Joomla zip installer (PHP 7.2 or higher)

`docker-compose run php-npm npm run watch` - for watching changes in the JS when developing

## Installing and Set up

After running the build the install package will be created in the `dist` folder.