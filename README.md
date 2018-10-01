:warning: The SFTP service provider is present natively in Laravel since [v5.6.7](https://github.com/laravel/framework/releases/tag/v5.6.7). You should avoid using this package if you are in a version of Laravel higher than this one.

[![Latest Stable Version](http://img.shields.io/github/release/neoxia/laravel-sftp.svg)](https://packagist.org/packages/neoxia/laravel-sftp)

## Laravel SFTP

This package provide a service provider to add the "sftp" driver to Laravel Storage.

## Installation

Require this package with composer using the following command:

```
composer require neoxia/laravel-sftp
```
## Notice

As of *Laravel 5.5*, this package will be automatically discovered and registered.
For older version of Laravel, add the service provider in `config/app.php`.

```PHP
Neoxia\Filesystem\SftpServiceProvider::class,
```

## Configuration

To configure a new Laravel storage disk on SFTP, provide a configuration like this one in `config/filesystems.php`

```PHP
'disks' => [

    'sftp' => [
        'driver'     => 'sftp',
        'host'       => env('SFTP_HOST', ''),
        'port'       => env('SFTP_PORT', '21'),
        'username'   => env('SFTP_USERNAME', ''),
        'password'   => env('SFTP_PASSWORD', ''),
        'privateKey' => env('SFTP_PRIVATE_KEY_PATH', ''),
        'root'       => env('SFTP_ROOT', ''),
        'timeout'    => env('SFTP_TIMEOUT', '10'),
    ],

],
```

## Licence

MIT Licence. Refer to the [LICENSE](https://github.com/neoxia/laravel-sftp/blob/master/LICENSE.md) file to get more info.
