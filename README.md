<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## Laravel Installer package


### Step - 1:
	
	<p> env file add this code</p>
	<code>APP_INSTALL=NO</code>
	

### Step -2: 
<p>Add provider file </br>
Laravel 11:</br>
bootstrap/providers.php</br>

Or</br>

Laravel < 11</br>
config/app.php</br>

Add this file</p>
	
<code>Codersgift\Installer\InstallerServiceProvider::class,</code>

### Step - 3:
<p>composer.json file</p>
<code>
"autoload-dev": {
      	      "psr-4": {
           		"Tests\\": "tests/",
           		"Codersgift\\Installer\\": "package/Installer/src/"
       	      }
   	},
</code>

	
### Step - 3: Publish the Assets
<p>
php artisan vendor:publish --tag=installer-assets </br>
This will copy the assets to public/install/css.
</p>


### Step - 4 : if you choose fresh data you have the available Setting model
<p>
Step for fresh data </br>
The user create so user table 
</p>

<code>
$table->foreignId('role_id')->default(2);
$table->boolean('status')->default(false);
</code>
