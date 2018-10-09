yii2-prototype
==============

Prototype emulator for Yii2 component

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist mdmsoft/yii2-prototype "~1.0"
```

or add

```
"mdmsoft/yii2-prototype": "~1.0"
```

to the require section of your `composer.json` file.


Usage
-----

```php
Yii::$app->attachBehavior(0,\mdm\prototype\Prototype::className());

Yii::$app->prototype->x = 1;
echo Yii::$app->x; // 1
Yii::$app->x = 'seratus';
echo Yii::$app->x; // 'seratus'

Yii::$app->prototype->z = function($var){
    echo $var;
};

Yii::$app->z('Hello cak');
 
Yii::$app->prototype->getSomething = function(){
    return 'something';
};

Yii::$app->something;
```
