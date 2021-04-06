<!-- Need a picture -->
##WELCOME！

## Table of contents

* [Overview](#overview)
* [Installation](#installation)
* [User Guide](#user-guide)
* [Community Feedback](#community-feedback)
* [Developer Guide](#developer-guide)
* [Development History](#development-history)
* [Team](#team)

## Overview

The Manoa Munchie app enables you to login on your phone and determine:

* What specific menu items will be available today at campus center locations.
* What food is available right now.
* When a style of food you love is available today.

## Installation

First, [install Meteor](https://www.meteor.com/install).

Second, download a copy of [Digits](https://github.com/sulao1999/digits/tree/master). Note that Digits is a private repo and so you will need to request permission from the author to gain access to the repo.

Third, cd into the app directory install the required libraries with:

```
$ meteor npm install
```

Once the libraries are installed, you can run the application by invoking:

```
$ meteor npm run start
```

The first time you run the app, it will create some default users and data. Here is the output:

```
meteor npm run start

> meteor-application-template-react@ start \Users\github\manoa-hungry-helper.github.io\app
> meteor --no-release-check --exclude-archs web.browser.legacy,web.cordova --settings ../config/settings.development.json

[[[[[ \Users\github\manoa-hungry-helper.github.io\app ]]]]]

=> Started proxy.
=> Started MongoDB.
W20210402-15:39:02.091(-10)? (STDERR) Note: you are using a pure-JavaScript implementation of bcrypt.
W20210402-15:39:02.218(-10)? (STDERR) While this implementation will work correctly, it is known to be
W20210402-15:39:02.219(-10)? (STDERR) approximately three times slower than the native implementation.
W20210402-15:39:02.219(-10)? (STDERR) In order to use the native implementation instead, run
W20210402-15:39:02.220(-10)? (STDERR)
W20210402-15:39:02.221(-10)? (STDERR)   meteor npm install --save bcrypt
W20210402-15:39:02.221(-10)? (STDERR)
W20210402-15:39:02.222(-10)? (STDERR) in the root directory of your application.
I20210402-15:39:10.123(-10)? Creating the default user(s)
I20210402-15:39:10.123(-10)?   Creating user admin@foo.com.
I20210402-15:39:10.568(-10)?   Creating user john@foo.com.
I20210402-15:39:10.850(-10)? Creating default contacts.
I20210402-15:39:10.851(-10)?   Adding: Johnson (john@foo.com)
I20210402-15:39:10.998(-10)?   Adding: Casanova (john@foo.com)
I20210402-15:39:11.000(-10)?   Adding: Binsted (admin@foo.com)
I20210402-15:39:11.585(-10)? Monti APM: completed instrumenting the app
=> Started your app.

=> App running at: http://localhost:3000/
   Type Control-C twice to stop.
```

### Note regarding "bcrypt warning":

```
W20210402-15:39:02.091(-10)? (STDERR) Note: you are using a pure-JavaScript implementation of bcrypt.
W20210402-15:39:02.218(-10)? (STDERR) While this implementation will work correctly, it is known to be
W20210402-15:39:02.219(-10)? (STDERR) approximately three times slower than the native implementation.
W20210402-15:39:02.219(-10)? (STDERR) In order to use the native implementation instead, run
W20210402-15:39:02.220(-10)? (STDERR)
W20210402-15:39:02.221(-10)? (STDERR)   meteor npm install --save bcrypt
W20210402-15:39:02.221(-10)? (STDERR)
W20210402-15:39:02.222(-10)? (STDERR) in the root directory of your application.
```

On some operating systems (particularly Windows), installing bcrypt is much more difficult than implied by the above message. Bcrypt is only used in Meteor for password checking, so the performance implications are negligible until your site has very high traffic. You can safely ignore this warning without any problems during initial stages of development.

If all goes well, the template application will appear at [http://localhost:3000](http://localhost:3000). You can login using the credentials in [settings.development.json](https://github.com/ics-software-engineering/meteor-application-template-react/blob/master/config/settings.development.json), or else register a new account.

## User Interface Walkthrough

### Landing Page

