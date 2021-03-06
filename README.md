Google Tag Manager extension for the Yii2 framework
===================================================
Integration Google Tag Manager in your application

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist ezoterik/yii2-google-tag-manager "*"
```

or add

```
"ezoterik/yii2-google-tag-manager": "*"
```

to the require section of your `composer.json` file.


Usage
-----

0. Add this code in your *@app/config/main.php* config file  with the other previous config:
 ```php
 'bootstrap' => ['googleTagManager'],
 'components' => [
     'googleTagManager' => [
         'class' => 'ezoterik\googleTagManager\GoogleTagManager',
         'tagManagerId' => 'GOOGLE_TAG_MANAGER_ID', //Your Google Tag Manager ID without "GTM-" prefix
     ],
 ],
 ```

0. You can generate events:
 ```php
 Yii::$app->googleTagManager->dataLayerPushItemDelay('event', 'example_event');
 ```
