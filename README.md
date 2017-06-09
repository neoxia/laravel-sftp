[![Latest Stable Version](http://img.shields.io/github/release/neoxia/laravel-sftp.svg)](https://packagist.org/packages/neoxia/laravel-sftp)

## Laravel SFTP

This package provide a service provider to add the "sftp" driver to Laravel Storage.

## Installation

In order to install this package, add `neoxia/laravel-sftp` in `composer.json`.

```JS
"require": {
    "neoxia/laravel-sftp": "1.0.*"
},
```

And add the service provider in `config/app.php`.

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
        'password'   => env('SFTP_PASSSWORD', ''),
        'privateKey' => env('SFTP_PRIVATE_KEY_PATH', ''),
        'root'       => env('SFTP_ROOT', ''),
        'timeout'    => env('SFTP_TIMEOUT', '10'),
    ],

],
```
