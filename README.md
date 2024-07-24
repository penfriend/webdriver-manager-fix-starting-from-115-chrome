
Webdriver Manager [![CircleCI Status](https://circleci.com/gh/angular/webdriver-manager.svg?style=shield)](https://circleci.com/gh/angular/webdriver-manager) [![Join the chat at https://gitter.im/angular/webdriver-manager](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/angular/webdriver-manager?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
=================

A selenium server and browser driver manager for your end to end tests with a fix to solve the issue starting from 115 chrome. To use it in protractor please install the package protractor-fix-starting-from-115-chrome. Here is more information about the changes from 115 chrome: https://developer.chrome.com/docs/chromedriver/downloads/version-selection. This is the same tool as `webdriver-manager` from the [Protractor](https://github.com/angular/protractor) repository.


**Note:** Version 9 and lower please reference [pose/webdriver-manager](https://github.com/pose/webdriver-manager). If there are features that existed in version 9 and lower, please open up an issue with the missing feature or a create a pull request.

Getting Started
---------------

```
npm install -g webdriver-manager-fix-starting-from-115-chrome

```

Setting up a Selenium Server
----------------------------

Prior to starting the selenium server, download the selenium server jar and driver binaries. By default it will download the selenium server jar and chromedriver binary.

```
node ./node_modules/protractor-fix-starting-from-115-chrome/bin/webdriver-manager update

```

Starting the Selenium Server
----------------------------

By default, the selenium server will run on `http://localhost:4444/wd/hub`.


```
node ./node_modules/protractor-fix-starting-from-115-chrome/bin/webdriver-manager start
```

Other useful commands
---------------------

View different versions of server and driver files:

```
node ./node_modules/protractor-fix-starting-from-115-chrome/bin/webdriver-manager status
```

Clear out the server and driver files. If `webdriver-manager start` does not work, try to clear out the saved files.

```
node ./node_modules/protractor-fix-starting-from-115-chrome/bin/webdriver-manager clean
```

Running / stopping server in background process (stopping is not yet supported on standalone server 3.x.x):

```
node ./node_modules/protractor-fix-starting-from-115-chrome/bin/webdriver-manager start --detach
node ./node_modules/protractor-fix-starting-from-115-chrome/bin/webdriver-manager shutdown
```

Help commands
-------------

Wedriver-manager has a main help option: `webdriver-manager help`. There are also other built in help menus for each of the commands. So for example, if you would like to look up all the flag options you can set in `update`, you could run `webdriver-manager update help`.

Here are a list of all the commands with help:

```
node ./node_modules/protractor-fix-starting-from-115-chrome/bin/webdriver-manager update help
node ./node_modules/protractor-fix-starting-from-115-chrome/bin/webdriver-manager start help
node ./node_modules/protractor-fix-starting-from-115-chrome/bin/webdriver-manager clean help
node ./node_modules/protractor-fix-starting-from-115-chrome/bin/webdriver-manager status help
```

Other topics:
--------------

- [mobile browser support](docs/mobile.md)
- [protractor support](docs/protractor.md)
- [set specific versions](docs/versions.md)