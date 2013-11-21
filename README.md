
# Hoodie - command line utility

[![NPM](https://nodei.co/npm/hoodie-cli.png?downloads=true&stars=true)](https://nodei.co/npm/hoodie-cli/)

[![Build Status](https://travis-ci.org/hoodiehq/hoodie-cli.png)](https://travis-ci.org/hoodiehq/hoodie-cli)
[![Dependency Status](https://david-dm.org/hoodiehq/hoodie-cli.png)](https://david-dm.org/hoodiehq/hoodie-cli)
[![devDependency Status](https://david-dm.org/hoodiehq/hoodie-cli/dev-status.png)](https://david-dm.org/hoodiehq/hoodie-cli#info=devDependencies)


The [Hoodie](http://hood.ie) CLI.

## Installation
Please ensure you have [node](http://nodejs.org) installed.

```
npm install -g hoodie-cli
```

## Usage

```
Usage: hoodie <command> <parameters>

Description:

  Hoodie command-line tool.

Commands:

  new <appname> [<template>]       create a hoodie project
  start                            start hoodie app
  install <plugin(s)>              install hoodie plugin
  uninstall <plugin(s)>            uninstall hoodie plugin

Options:

  -h, --help           output usage information
  
```

for more in-depth usage info you can run: `hoodie <command> -h`

### Getting started

##### hoodie start

```
hoodie new my-hoodie-app
```
Creates a new hoodie app inside a new folder called `my-hoodie-app`. If you don't specify a name `my-first-hoodie` is set as app name.

If the `new` command has been successful you should be seeing:

```
You can now start using your hoodie app

  cd my-hoodie-app
  hoodie start
```

So let's run `hoodie start`:

```
.d$b.  .d$b.  .d$$$$$$b.    .d$$$$$$b.  .d$$$$$$b.  .d$b..d$$$$$$$$b.
$$$$$..$$$$$.$$$$$$$$$$$b .$$$$$$$$$$$b $$$$$$$$$$b $$$$$$$$$$$$$$$P'
$$$$$$$$$$$$d$$$$$$$$$$$$bd$$$$$$$$$$$$b$$$$$$$$$$$b$$$$$$$$$$$$$$$b.
$$$$$$$$$$$$Q$$$$$$$$$$$$PQ$$$$$$$$$$$$P$$$$$$$$$$$P$$$$$$$$$$$$$$$P'
$$$$$´`$$$$$'$$$$$$$$$$$$''$$$$$$$$$$$$'$$$$$$$$$$P $$$$$$$$$$$$$$$b.
'Q$P'  'Q$P'  'Q$$$$$$P'    'Q$$$$$$P'  'Q$$$$$$$P  'Q$P''Q$$$$$$$$P'

Version: 0.3.2 (node v0.10.20, npm 1.3.14, platform: darwin)

Initializing...
CouchDB started: http://127.0.0.1:6045
Waiting for CouchDB [----*-] SUCCESS
prompt: Please set an admin password: // the bit were you should be entering a password
WWW:   http://127.0.0.1:6043
Admin: http://127.0.0.1:6044
Starting Plugin: 'hoodie-plugin-email'
Starting Plugin: 'hoodie-plugin-users'
All plugins started.

```

##### hoodie install / uninstall

As you can see above, we install a number of plugins by default. Namely 'hoodie-plugin-email` and `hoodie-plugin-users`:

```
…
Starting Plugin: 'hoodie-plugin-email'
Starting Plugin: 'hoodie-plugin-users'
…
```
If you would like to install you're own plugins, you can run:

```
hoodie install hoodie-plugin-fancy
```

and to uninstall:

```
hoodie uninstall hoodie-plugin-fancy
```
