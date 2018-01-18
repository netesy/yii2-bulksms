A simple class to handle the bulk sms api for Nigerian bulk sms hhtp api connection
===================================================================================
A simple class to handle the bulk sms api for Nigerian bulk sms hhtp api connection

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist netesy/yii2-bulksms "*"
```

or add

```
"netesy/yii2-bulksms": "*"
```

to the require section of your `composer.json` file.


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
          'sender' => 'sender',
          'url' => 'http://portal.nigerianbulksms.com/api/',
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