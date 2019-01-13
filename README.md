[![Netesy](https://img.shields.io/scrutinizer/g/filp/whoops.svg)](https://www.github.com/netesy)
[![Netesy](https://img.shields.io/github/languages/code-size/badges/shields.svg)](https://www.github.com/netesy)
[![Yii2](https://img.shields.io/badge/Powered_by-Yii_Framework-green.svg?style=flat)](https://www.yiiframework.com/)

A Yii2 extension to handle sending messages for most Nigerian bulksms http api connections
===================================================================================
A Yii2 extension to handle sending messages for most Nigerian bulksms http api connections

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer require netesy/yii2-bulksms
```

or add

```
"netesy/yii2-bulksms": "*"
```

to the require section of your `composer.json` file.


Supported websites
-----
[NigerianBulkSMS](http://nigerianbulksms.com/)

[BetaSMS](http://betasms.com/)


Usage
-----

Once the extension is installed, simply use it in your code by  :

<!-- ```php
<?= \netesy\bulksms\AutoloadExample::widget(); ?>```
 -->
first add to config.php
```php
<?php
'components' => [
	'bulksms' => [
          'class' => 'netesy\bulksms\BulkSms',
          'username' => 'xxxxxxxx',
          'password' => 'xxxxxxxx',
          'sender' => 'sender number',
          'url' => 'the api address',
          ],
]
?>
```

Once the extension is installed, simply use it in your code by  :
to send a message
```php
<?php 
	Yii::$app->bulksms->sendMessage([
    'number' => $number,
    'message' => 'message',
      ]);
 ?>
```
to send a call
```php
<?php 
	Yii::$app->bulksms->sendCall([
    'number' => $number,
    'message' => 'message',
      ]);
 ?>
```

to get your account balance

```php
<?php 
	Yii::$app->bulksms->getBalance();
 ?>
```
