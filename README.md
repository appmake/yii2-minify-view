Yii 2 Minify View Component
===========================

# Installation

The preferred way to install this extension is through composer.

Either run

```
php composer.phar require --prefer-dist appmake/yii2-minify-view "*"
```

or add

```
"appmake/yii2-minify-view": "*"
```

Configure
---------
```php
<?
return [
	// ...
	'components' => [
		// ...
		'view' => [
			'class' => '\rmrevin\yii\minify\View',
			'enableMinify' => !YII_DEBUG,
			'web_path' => '@web', // path alias to web base
			'base_path' => '@webroot', // path alias to web base
			'minify_path' => '@webroot/minify', // path alias to save minify result
			'js_position' => [ \yii\web\View::POS_END ], // positions of js files to be minified
			'force_charset' => 'UTF-8', // charset forcibly assign, otherwise will use all of the files found charset
			'expand_imports' => true, // whether to change @import on content
			'compress_output' => true, // compress result html page
		]
	]
];
```
