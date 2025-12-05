# 通过 DM8 为 Laravel 提供的 DM 数据库驱动

## Laravel-DM8

Laravel-DM8 是一个适用于 Laravel 的 Dm 数据库驱动包。Laravel-DM8 是 Illuminate/Database 的一个扩展，使用 DM8 扩展与 Dm 进行通信。感谢 @yajra。

## Documentations

- 您可以在这里找到用户友好且更新的文档：[Laravel-DM8 文档](https://github.com/595708049/laravel-dm8)
- 关于 dm 和 php 的所有内容：[ PHP 和 Dm 手册](https://eco.dameng.com/document/dm/zh-cn/app-dev/php-php.html)

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

一旦 Composer 安装或更新了你的软件包，你需要注册 Laravel-DM8。打开 `config/app.php`，找到 providers 键并添加：

```php
LaravelDm8\Dm8\Dm8ServiceProvider::class,
```

## Configuration (OPTIONAL)

最后，您可以通过运行以下 Artisan 命令选择性地发布配置文件。如果配置文件未发布，包将自动使用您 `.env` 文件中声明的数据库配置。

这将把配置文件复制到 `config/database.php`。

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
