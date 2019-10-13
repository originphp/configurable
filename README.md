# Configurable

![license](https://img.shields.io/badge/license-MIT-brightGreen.svg)
[![build](https://travis-ci.org/originphp/configurable.svg?branch=master)](https://travis-ci.org/originphp/configurable)
[![coverage](https://coveralls.io/repos/github/originphp/configurable/badge.svg?branch=master)](https://coveralls.io/github/originphp/configurable?branch=master)

Configurable traits to add default config and setters and getters.

## Installation

To install this package

```linux
$ composer require originphp/configurable
```


## Usage

Both instance and static traits are available.

Set `defaultConfig` property

```php
use Origin\Configurable\InstanceConfigurable as Configurable;

class MyObject
{
    use Configurable;

    protected $defaultConfig = [
        'foo' => 'bar'
    ];
}
```


To get a value from the config:

```php
 $value = $this->config('foo'); // bar
```

To all of the values from the config

```php
 $array = $this->config();
```

To set a value in the config:

```php
 $this->config('foo','bar');
 $this->config(['foo'=>'bar']);
```

To set multiple values (merges config)

```php
 $this->config(['foo'=>'bar']);
```
