## Simple Administrator Package for Laravel 5

[![Build Status](https://travis-ci.org/pingpong-labs/admin.svg?branch=master)](https://travis-ci.org/pingpong-labs/admin)
[![Latest Stable Version](https://poser.pugx.org/pingpong/admin/v/stable.svg)](https://packagist.org/packages/pingpong/admin) [![Total Downloads](https://poser.pugx.org/pingpong/admin/downloads.svg)](https://packagist.org/packages/pingpong/admin) [![Latest Unstable Version](https://poser.pugx.org/pingpong/admin/v/unstable.svg)](https://packagist.org/packages/pingpong/admin) [![License](https://poser.pugx.org/pingpong/admin/license.svg)](https://packagist.org/packages/pingpong/admin)
[![HHVM Status](http://hhvm.h4cc.de/badge/pingpong/admin.svg)](http://hhvm.h4cc.de/package/pingpong/admin)

### Server Requirements

- PHP 5.4 or higher

### What's New

- Admin theme now using [AdminLTE](https://github.com/almasaeed2010/AdminLTE)

### Installation

> For Laravel 4, use version `~1`.

Open your composer.json file, and add the new required package.
```
"pingpong/admin": "dev-develop" 
```

Next, open a terminal and run.
```
composer update 
```

Next, Add new service provider in `app/config/app.php`.

```php
'Pingpong\Admin\Providers\SupportServiceProvider',
'Pingpong\Admin\AdminServiceProvider',
```

Next, update your user model to extend the `Pingpong\Admin\Entities\User` class. Looks like this.

```php
// app/User.php

class User extends \Pingpong\Admin\Entities\User {}
```

Next, publish the package's config and assets.
```
php artisan vendor:publish --package="Pingpong\Admin\AdminServiceProvider"
```

Next, install the package.
```
php artisan admin:install
```

Done.

### Screenshot

[![Build Status](https://raw.githubusercontent.com/pingpong-labs/admin/master/shots/pingpong-admin-shot.png)](https://raw.githubusercontent.com/pingpong-labs/admin/master/shots/pingpong-admin-shot.png)

### Usage

Browse your app to the url : `http://your-host.com/admin`. By default the login credentials is `pingpong.labs@gmail` for the email and `secret` for the password.

### Documentation

For more documentation please see [wiki](https://github.com/pingpong-labs/admin/wiki) part of this repo.

### License

This package is open-sourced software licensed under [The BSD 3-Clause License](http://opensource.org/licenses/BSD-3-Clause)
