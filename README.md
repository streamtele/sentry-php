# sentry-php

[![Build Status](https://travis-ci.org/immobiliare/sentry-php.svg?branch=master)](https://travis-ci.org/immobiliare/sentry-php)
[![Latest Stable Version](https://poser.pugx.org/immobiliare/sentry-php/v/stable?style=flat-square)](https://packagist.org/packages/immobiliare/sentry-php)
[![Total Downloads](https://poser.pugx.org/immobiliare/sentry-php/downloads?style=flat-square)](https://packagist.org/packages/immobiliare/sentry-php)
[![Latest Unstable Version](https://poser.pugx.org/immobiliare/sentry-php/v/unstable?style=flat-square)](https://packagist.org/packages/immobiliare/sentry-php)
[![License](https://poser.pugx.org/immobiliare/sentry-php/license?style=flat-square)](https://packagist.org/packages/immobiliare/sentry-php)
[![Monthly Downloads](https://poser.pugx.org/immobiliare/sentry-php/d/monthly?style=flat-square)](https://packagist.org/packages/immobiliare/sentry-php)
[![Daily Downloads](https://poser.pugx.org/immobiliare/sentry-php/d/daily?style=flat-square)](https://packagist.org/packages/immobiliare/sentry-php)

This project is a fork of official [PHP SDK v1.7](https://github.com/getsentry/sentry-php) for [Sentry](https://getsentry.com) to work even with php5.2, php5.6
This project already have fix for https://github.com/getsentry/sentry-php/pull/615/commits/21e39a6bc4e27591dabe4118d9b996bbc109b3a0

## Features

- Automatically report (un)handled exceptions and errors
- Send customized diagnostic data
- Process and sanitize data before sending it over the network

## Installation

There are various ways to install the PHP integration for Sentry.  The
recommended way is to use [Composer](http://getcomposer.org).

    $ composer require fly304625/sentry-php:1.7.x-dev

Alternatively you can manually install it:

1.  Download and extract the latest [sentry-php](https://github.com/fly304625/sentry-php/archive/master.zip) archive to your PHP project.
2.  Require the autoloader in your application:

```php
require_once '/path/to/Raven/library/Raven/Autoloader.php';
Raven_Autoloader::register();
```

## Usage

```php
// Instantiate a new client with a compatible DSN and install built-in
// handlers
$sentryClient = new Raven_Client('https://e9ebbd88548a441288393c457ec90441:399aaee02d454e2ca91351f29bdc3a07@app.getsentry.com/3235');
$sentryClient->install();

// Capture an exception
$event_id = $sentryClient->captureException($ex);

// Give the user feedback
echo "Sorry, there was an error!";
echo "Your reference ID is " . $event_id;
```

For more information, see the [documentation](https://docs.getsentry.com/hosted/clients/php/).


## Integration with frameworks

Other packages exists to integrate this SDK into the most common frameworks.

- [Symfony](https://github.com/getsentry/sentry-symfony)
- [Laravel](https://github.com/getsentry/sentry-laravel)


## Community

- [Documentation](https://docs.getsentry.com/hosted/clients/php/)
- [Bug Tracker](http://github.com/immobiliare/sentry-php/issues)
- [Code](http://github.com/immobiliare/sentry-php)


Contributing
------------

Dependencies are managed through composer:

```
$ composer install
```

Tests can then be run via phpunit:

```
$ vendor/bin/phpunit
```
