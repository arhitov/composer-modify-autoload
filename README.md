# composer-modify-autoload

Updates the vendor/autoload.php so it manually includes any files specified in composer.json's files array.
See https://github.com/composer/composer/issues/6768

## composer.json

Files that need to be included at the very beginning
```
{
 // ... 
  "autoload": {
    "priority": [
      "your_file.php"
    ]
  }
 // ...
}
```

Autorun script after composer update
```
{
 // ... 
  "scripts": {
    "post-autoload-dump": [
      "php modify_autoload.php"
    ]
  }
 // ...
}
```
