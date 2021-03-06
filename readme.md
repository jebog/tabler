# Laravel Tabler Bootstrap 4
Laravel 7.0 and 8.0 Package for integrating Tabler template and this package is Laravel Mix friendly. Currently this package can be integrated easily only on fresh installation.

# Pre-Installation
Before install, you must create the authentication scaffolding manually

```
  1. First install laravel/ui package from composer  
     ```php
     composer require laravel/ui
     ```
  1. And then, run code below
     ```php
     php artisan ui vue --auth
     ```

# Installation
```php
composer require jebog/tabler
```
Run this code below to implement the template,
```php
php artisan make:tabler
```
Let's see what we've installed. First, make sure that you've already ran ```php artisan migrate``` command, then do
```php
php artisan serve
```
Viola! a Laravel site using Tabler is running right now.

# Configuration and Views Customization
## Config
To publish this package config to your app config, run this code below
```php
php artisan vendor:publish --provider="Jebog\Tabler\Providers\AppServiceProvider" --tag="config"
```
## Views
To publish this package views so you can customize on your own, run this code below
```php
php artisan vendor:publish --provider="Jebog\Tabler\Providers\AppServiceProvider" --tag="views"
```

# Next Step
First of all, you should understand how to use [Laravel Mix](https://laravel.com/docs/mix) and install latest laravel-mix.

Tabler need some package on npm. First you need to run
```php
npm install
```

Install Tabler needed package from npm
```php
npm install --save-dev bootstrap bootstrap-sass popper.js chart.js d3 font-awesome jquery-circle-progress jvectormap moment requirejs select2 select2-bootstrap-theme selectize sparkline tabler-ui tablesorter bootstrap-datepicker eonasdan-bootstrap-datetimepicker @ttskch/select2-bootstrap4-theme
```

Run Laravel Mix command
```php
npm run development
```
or use ```production``` minimize output
```php
npm run production
```

Then have a good look on these files
- ```webpack.mix.js```
- ```resources/assets/js/tabler.js```
- ```resources/assets/sass/tabler.scss```

Happy experimenting!
