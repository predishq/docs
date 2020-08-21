## How to install [Predis](https://github.com/predis/predis)?

* Using [Composer](http://packagist.org/about-composer):
```cmd
$ composer require predis/predis
```

Or add it to your `composer.json`:
```json
{
    "require": {
            "predis/predis": "v1.1.x-dev"
    }
}
```

Then you run:
```cmd
$ composer update
```

----------

* Without Composer:

You can clone the library into your project:
```cmd
$ git clone git://github.com/predis/predis.git
```

Predis relies on the autoloading features of PHP to load it is files when needed and complies with the [PSR-4 standard](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md).
Autoloading is handled automatically when dependencies are managed through composer, but it is also possible to leverage it is own autoloader in
projects or scripts lacking any autoload facility.
So, after cloning the library you can load it by:
```php
// Prepend a base path if Predis is not available in your "include_path".
require 'Predis/Autoloader.php';

Predis\Autoloader::register();
```