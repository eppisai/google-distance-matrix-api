# Google Distance Matrix API
Estimate travel time and distance for multiple destinations.

Requirements
============
Requires PHP 7.1 or higher.
Composer setup

WHAT IS COMPOSER : 
Composer is an application-level package manager for the PHP programming language that provides a standard format for managing dependencies of PHP software and required libraries. It also allows users to install PHP applications that are available on "Packagist" ,  which is its main repository containing available packages

Composer offers several parameters including :

require: add the library in parameter to the file composer.json, and install it.
install: install all libraries from composer.json. It's the command to use to download all PHP repository dependencies.
update: update all libraries from composer.json, according to the allowed versions mentioned into it.
remove: uninstall a library and remove it from composer.json.

Installation
=============

The best way to install finalbytes/google-distance-matrix-api is using  [Composer](http://getcomposer.org/):

```sh
$ composer require finalbytes/google-distance-matrix-api
```

Getting Started
===============

```php

$distanceMatrix = new GoogleDistanceMatrix('YOUR API KEY');
$distance = $distanceMatrix
    ->setLanguage('nl-NL')
    ->addOrigin('51.458428,6.0541768')
    ->addDestination('48.139212,11.581721')
    ->addDestination('36.721184,-4.420084')
    ->sendRequest();

```

```php
$distanceMatrix = new GoogleDistanceMatrix('YOUR API KEY');
$distance = $distanceMatrix
    ->addOrigin('Van Bronckhorststraat 94, 5961SM Horst, The Netherlands')
    ->addDestination('Maistraße 10, 80337 München, Deutschland')
    ->setMode(GoogleDistanceMatrix::MODE_DRIVING)
    ->setLanguage('nl-NL')
    ->setUnits(GoogleDistanceMatrix::UNITS_METRIC)
    ->setAvoid(GoogleDistanceMatrix::AVOID_FERRIES)
    ->sendRequest();
```
    
For more info, please visit https://developers.google.com/maps/documentation/distance-matrix/
