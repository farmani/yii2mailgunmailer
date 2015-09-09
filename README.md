Yii2 Mailgun Mailer
===================
Mailgun mailer for Yii 2 framework.

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist farmani/yii2mailgunmailer "*"
```

or add

```
"farmani/yii2mailgunmailer": "*"
```

to the require section of your `composer.json` file.


Config
-----

```php
'components' => [
		...
		'mailer' => [
				'class' => 'farmani\yii2mailgunmailer\Mailer',
				'domain' => 'example.com',
				'key' => 'key-somekey',
				'tags' => ['yii'],
				'enableTracking' => false,
		],
		...
],
?>```

Usage
-----

Once the extension is installed, simply use it in your code by  :

```php
<?php
Yii::$app->mailer->compose('<view_name>', <option>)
->setFrom("<from email>")
->setTo("<to email>")
->setSubject("<subject>")
// ->setHtmlBody("<b> Hello User </b>")
// ->setTextBody("Hello User")
->send();
?>```