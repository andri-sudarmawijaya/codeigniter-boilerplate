# Codegniter Boilerplate

##  install codeigniter
```bash
composer create-project andri-sudarmawijaya/codeigniter-composer-installer codeigniter-boilerplate
```
### set your base_url in config.php
```php
$config['base_url'] = ((isset($_SERVER['HTTPS']) && $_SERVER['HTTPS'] == "on") ? "https" : "http");
$config['base_url'] .= "://" . $_SERVER['HTTP_HOST'];
$config['base_url'] .= str_replace(basename($_SERVER['SCRIPT_NAME']), "", $_SERVER['SCRIPT_NAME']);
```
### set your database in database.php
```php
	'username' => 'YOUR-DATABASE-USER',
	'password' => 'YOUR-DATABASE-PASSWORD',
	'database' => 'YOUR-DABASE-NAME',
```

## Install smartyacl
```bash
composer require andri-sudarmawijaya/smartyacl:1.0.x-dev
```

### Set autoload in autoload.php
In application/config/autoload.php

Add to $autoload['packages']¹
```php
$autoload['packages'] = array(APPPATH.'third_party/SmartyAcl');
```
Add to $autoload['helper']¹
```php
$autoload['helper'] = array('url');
```
Add to $autoload['libraries']¹
```php
$autoload['libraries'] = array('form_validation');
```

### Import DB tables
Import using migration or database.sql file from [Smarty ACL](https://github.com/rubensrocha/codeigniter-smarty-acl).

## Install theme
```bash
composer require andri-sudarmawijaya/coreui-smarty-acl:1.0.x-dev
```
### run the script
```bash
composer run-script post-update-cmd -d vendor/andri-sudarmawijaya/coreui-smarty-acl
```



