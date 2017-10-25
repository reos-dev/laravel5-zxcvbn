# Laravel Zxcvbn validator

This package providers a validator which uses dropbox's [zxcvbn](https://github.com/dropbox/zxcvbn) 
password strength estimator; it uses the [PHP implementation](https://github.com/bjeavons/zxcvbn-php) from
[bjeavons](https://github.com/bjeavons). 

## Installation

This package can be installed through Composer.

``` bash
composer require rebelinblue/laravel5-zxcvbn
```

In Laravel 5.5 the package will auto-register the service provider. In Laravel 5.4 you must register this 
service provider manually in `config/app.php` by adding `REBELinBLUE\Zxcvbn\ZxcvbnServiceProvider::class` to the 
`providers` array


There is also an optional facade for Zxcvbn; in Laravel 5.5 it will be auto-registered. In Laravel 5.4
you must register the facade manually by adding the following to the `aliases` array in `config/app.php`

```php
    'Zxcvbn' => REBELinBLUE\Zxcvbn\ZxcvbnFacade::class,
```

Optionally, you can publish the translations for this package with, however it is only required if you wish to change them

``` bash
php artisan vendor:publish --provider="REBELinBLUE\Zxcvbn\ZxcvbnServiceProvider"
```