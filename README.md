# [reCaptcha checker](https://github.com/Shaneen31/recaptchachecker)
[Version 1.0.0](https://github.com/Shaneen31/recaptchachecker/releases/tag/v1.0.0)

Easy to use reCaptcha class for php projects.
No dependencies needed!

### Usage
Register your website on the [reCaptcha website](https://www.google.com/recaptcha/admin)

Add the following code to your php file or controller:
```php
require_once('functions/recaptcha.php');
$recaptcha = new Recaptcha('your-site-key', 'your-secret-key');
```

To dynamically generate the html code add the following code:
Just above the closing <head> tag to include script
```php
<?= $recaptcha->script(); ?>
```

In the form where you want to display reCaptcha widget.
```php
<?= $recaptcha->script(); ?>
```

To check if the reCaptcha is valid add the following code to your view:
```php
if($recaptcha->isValid($_POST['g-recaptcha-response'], $_SERVER['REMOTE_ADDR']) === false){
    ... Send your error message to view;
} else {
    ... Continue form treatment;
}
```

### Contributing
We encourage you to contribute to this repository. To contribute fork, make your change and send a pull request.

### License
Code and documentation released under [GNU GPL V2](https://github.com/Shaneen31/recaptchachecker/blob/master/LICENSE)