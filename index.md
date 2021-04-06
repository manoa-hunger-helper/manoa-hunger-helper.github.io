
# TABLE OF CONTENTS
***
* [Overview](#overview)
* [Installation](#installation)
* [User Guide](#user-guide)
* [Community Feedback](#community-feedback)
* [Developer Guide](#developer-guide)
* [Development History](#development-history)
* [Team](#team)

# OVERVIEW
****
There are many food choices on campus: Campus Center, food trucks, Manoa Gardens, Paradise Palms, vending machines, and so forth. Let’s say you have a desire for chinese food today for lunch. What places on campus are serving chinese food menu items today? Alternatively, let’s say that you love the fresh salmon fillet at Campus Center, but that dish is only served once every few weeks. How do you find out on the day that it’s available?
Manoa-hunger-helper enables you to login on your phone and determine:

- What specific menu items will be available today at any Campus locations.
- What food is available right now.
- When a style of food you love is available today.

# TEAM 
***
 Four ICS students at the University of Hawaii at Manoa. 
 * [Yongxin yang](https://yongxinyang.github.io/)
 * [Feimei Chen](https://feimeichen.github.io/)
 * [Su Lao](https://sulao1999.github.io/)
 * [Jessica Ocampo](https://jnocampo.github.io/)

# INSTALLATION 

First, [install Meteor](https://www.meteor.com/install).

Second, download a copy of [manoa-hunger-helper](https://github.com/manoa-hunger-helper/manoa-hunger-helper).

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
W20210402-13:33:02.091(-10)? (STDERR) Note: you are using a pure-JavaScript implementation of bcrypt.
W20210402-13:33:02.218(-10)? (STDERR) While this implementation will work correctly, it is known to be
W20210402-13:33:02.219(-10)? (STDERR) approximately three times slower than the native implementation.
W20210402-13:33:02.219(-10)? (STDERR) In order to use the native implementation instead, run
W20210402-13:33:02.220(-10)? (STDERR)
W20210402-13:33:02.221(-10)? (STDERR)   meteor npm install --save bcrypt
W20210402-13:33:02.221(-10)? (STDERR)
W20210402-13:33:02.222(-10)? (STDERR) in the root directory of your application.
I20180227-13:33:02.716(-10)? Creating the default user(s)
I20180227-13:33:02.742(-10)?   Creating user admin@foo.com.
I20180227-13:33:02.743(-10)?   Creating user john@foo.com.
I20180227-13:33:02.743(-10)? Creating default data.
I20180227-13:33:02.743(-10)?   Adding: Basket (john@foo.com)
I20180227-13:33:02.743(-10)?   Adding: Bicycle (john@foo.com)
I20180227-13:33:02.743(-10)?   Adding: Banana (admin@foo.com)
I20180227-13:33:02.744(-10)?   Adding: Boogie Board (admin@foo.com)
I20180227-13:33:02.745(-10)? Monti APM: completed instrumenting the app
=> Started your app.

=> App running at: http://localhost:3000/
   Type Control-C twice to stop.
```

### Note regarding "bcrypt warning":

```
W20210402-13:33:02.091(-10)? (STDERR) Note: you are using a pure-JavaScript implementation of bcrypt.
W20210402-13:33:02.218(-10)? (STDERR) While this implementation will work correctly, it is known to be
W20210402-13:33:02.219(-10)? (STDERR) approximately three times slower than the native implementation.
W20210402-13:33:02.219(-10)? (STDERR) In order to use the native implementation instead, run
W20210402-13:33:02.220(-10)? (STDERR)
W20210402-13:33:02.221(-10)? (STDERR)   meteor npm install --save bcrypt
W20210402-13:33:02.221(-10)? (STDERR)
W20210402-13:33:02.222(-10)? (STDERR) in the root directory of your application.
```

On some operating systems (particularly Windows), installing bcrypt is much more difficult than implied by the above message. Bcrypt is only used in Meteor for password checking, so the performance implications are negligible until your site has very high traffic. You can safely ignore this warning without any problems during initial stages of development.

If all goes well, the template application will appear at [http://localhost:3000](http://localhost:3000). You can login using the credentials in [settings.development.json](https://github.com/manoa-hunger-helper/manoa-hunger-helper/blob/master/config/settings.development.json), or else register a new account.

# USER GUIDE

## [Landing Page](https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-Landing.jpg)

<img src= "https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-Landing.jpg">

## [Sign Up](https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Sign%20up.jpg)

<img src= "https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Sign%20up.jpg">

## [Sign In](https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-Sign-In.jpg)

<img src="https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-Sign-In.jpg">

## [User Homepage](https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-user.jpg)

<img src="https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-user.jpg">

 * [My Profile page](https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-MyProfile.jpg)
  
  <img src="https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-MyProfile.jpg">
  
 * [All Vendors page](https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-AllVendors.jpg)
 
 <img src="https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-AllVendors.jpg">
 
 * [Vendors Now Available page](https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-Vendors-available.jpg)
 
  <img src ="https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-Vendors-available.jpg">
  
 * [Today’s top picks page](https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-today-top-pick.jpg)
  
  <img src="https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-today-top-pick.jpg">
  
 * [Recommentdation page](https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-recommendation.jpg)

  <img src="https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-recommendation.jpg">
 
## [Vendor Homepage]()

 * [My Vendor page](https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-Vendor-My%20vendor.jpg)
 
 <img src="https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-Vendor-My%20vendor.jpg">
 
 * [All Vendors page](https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-AllVendors.jpg)
 
 <img src="https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-AllVendors.jpg">

## [Admin Homepage](https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-admin.jpg)

   <img src="https://github.com/manoa-hunger-helper/manoa-hunger-helper.github.io/blob/main/images/Hunger-Helper-admin.jpg">

 * [Manage users page]()
 * [Manage Vendors page]()

# DEVELOPMENT HISTORY

 * [M1](https://github.com/manoa-hunger-helper/manoa-hunger-helper/projects/1)
 * [M2]()
 * [M3]()
