# SmartyView - Laravel View Replacement #

SmartyView replaces the default Laravel View class with the 
[Smarty Template Engine](http://smarty.net/).

Included Smarty version: 3.1.13

## Installation ##

1. Download the Source from [Github](https://github.com/borissamardzija/Laravel-SmartyView/archive/master.zip).

2. Register the Bundle with Laravel
In the `application/bundles.php` file, register the SmartyView bundle
```php
'smartyview' => array(
  'location' => 'smartyview', 'autoloads' => array(
    'map' => array(
      'SmartyView\\View' => '(:bundle)/view.php',
    )
  )
)
```

3. Replace the View alias (optional)
In the `application/config/application.php` file, replace the alias with the following:
```php
'aliases' => array(
  ...
  View' => 'SmartyView\\View',
);
```

If you do not wish to replace or create the alias, you can use the Smarty template engine like this:

```php
// app view
\SmartyView\View::make('index.test')->with('var', 'value');

// bundle view
\SmartyView\View::make('docs::test')->with('var', 'value');
```


## Thanks ##
[Kris Geens] (https://github.com/skmedia) for [original](https://github.com/skmedia/Laravel-SmartyView) Laravel-SmartyView [bundle](http://bundles.laravel.com/bundle/SmartyView).
