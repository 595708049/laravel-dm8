# 通过 DM8 为 Laravel 提供的 DM 数据库驱动

## Laravel-DM8

Laravel-DM8 是一个适用于 Laravel 的 Dm 数据库驱动包。Laravel-DM8 是 Illuminate/Database 的一个扩展，使用 DM8 扩展与 Dm 进行通信。感谢 @yajra。

## Documentations

- 您可以在这里找到用户友好且更新的文档：[Laravel-DM8 文档](https://github.com/595708049/laravel-dm8)
- 关于 dm 和 php 的所有内容：[地下 PHP 和 Dm 手册](https://eco.dameng.com/document/dm/zh-cn/app-dev/php-php.html)

## Laravel Version Compatibility

 Laravel  | Package
:---------|:----------
 10.x.x   | 1.x.x
 11.x.x   | 1.x.x

## Quick Installation

```bash
composer require wangl/laravel-dm8
```

## Service Provider (Optional on Laravel 5.5+)

Once Composer has installed or updated your packages you need to register Laravel-DM8. Open up `config/app.php` and find the providers key and add:

```php
LaravelDm8\Dm8\Dm8ServiceProvider::class,
```

## Configuration (OPTIONAL)

Finally you can optionally publish a configuration file by running the following Artisan command.
If config file is not publish, the package will automatically use what is declared on your `.env` file database configuration.

This will copy the configuration file to `config/database.php`.

> Then, you can set connection data in your `.env` files:

```ini
 'connections' => [
        'mysql' => [
           …………
        ],

        'dm' => [
            'driver'         => 'dm',
            'host'           => env('DB_HOST', '127.0.0.1'),
            'port'           => env('DB_PORT', '5236'),
            'database'       => env('DB_DATABASE', 'laravel'),
            'username'       => env('DB_USERNAME', 'laravel'),
            'password'       => env('DB_PASSWORD', 'laravel'),
            'charset'        => 'UTF8',
            'collation'      => 'utf8_general_ci',
            'prefix'         => '',
            'strict'         => true,
            'engine'         => null,
            'options' => [
                \PDO::ATTR_PERSISTENT => true,
                \PDO::ATTR_ERRMODE => \PDO::ERRMODE_EXCEPTION,
            ],
        ],
    ],
```

Then run your laravel installation...

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[link-author]: https://github.com/595708049
