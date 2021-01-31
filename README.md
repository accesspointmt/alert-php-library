# alert-php-library

A PHP composer library for the Alert Payment Gateway.

Features
------------

1. Setup Features:
    - Get list of allowed Card Brands for a Bank Merchant Reference.
    - Get list of allowed Transaction Types for a Bank Merchant Reference.
    - Get application information for a Bank Merchant Reference and AppGUID.
    - Get list of supported currencies for a Bank Merchant Reference.

2. Transaction Features:
    - Processing Transactions with the Alert Payment Gateway, with/without 3D Secure.
    - Get Transactions with a transaction reference.
    - Get Tranasction History through transaction reference root and/or Bank Merchant Reference.

3. Card Storage Features:
    - Save a Card with reference to an AppGUID and Bank Merchant Reference, for a specified length of time.
    - Remove a Card with through CardGUID, with reference to an AppGUID and Bank Merchant Reference.
    - Update Card Information with reference to an AppGUID and Bank Merchant Reference, for a specified length of time.
    - Get list of stored Cards for a Bank Merchant Refereence and AppGUID, or with a list of CardGUID's

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist accesspoint/apg
```

or add

```
"accesspoint/apg": "1.0.0"
```

to the require section of your `composer.json` file.


Usage
-----

In order to use the library, an instance of class APGClient in namespace APG must be created. The APGClient has 2 distinct constructors:

APGClient(*filepath*, *referringURL*)
or
APGClient(*username*, *password*, *referringURL*)

The first makes use of the secure.apg file supplied when you register your system with the Alert Payment gateway. You can simply pass the local URL of you file in the first argument, and the referring URL in the second.

The second does not require the secure.apg file, but requires the username and password that can be found in this file. This can be used when the file cannot be hosted.

Once an instance of APGClient is created, all the functions found in the APG documentation are accessible directly through PHP. For in depth documentation of each function please follow the APG Documentation.