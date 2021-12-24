# Introduction

Lumen Horizon is based on the official [Laravel Horizon](https://github.com/laravel/horizon) (v5.x) package.
It provides the same features as original package except the UI.
Tested with **Lumen 8**

## Installation

1. Important!
   Uncomment in your `bootstrap/app.php`

```php
$app->withFacades();
$app->withEloquent();
```

Make sure you register `Illuminate\Redis\RedisServiceProvider::class` in your `boorstrap/app.php` file.

```php
    $app->register(Illuminate\Redis\RedisServiceProvider::class);
```

Add in your `bootstrap/app.php`

```php
$app->configure('app');
```

2. Run composer to add the dependency.

```bash
    composer require kingdarkness/lumen-horizon
```

3. Publish config
   add the `horizon.php` to config/horizon

```bash
    cp vendor/kingdarkness/horizon-lumen/config/horizon.php config/horizon.php
```

4. register provider in your `bootstrap/app.php`

```php
    // add provider
    $app->register(Laravel\Horizon\HorizonServiceProvider::class);
    // add config
    $app->configure('horizon');
```

## Official Documentation

Documentation for Horizon can be found on the [Laravel website](https://laravel.com/docs/horizon).
