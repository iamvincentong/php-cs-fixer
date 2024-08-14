## Requirements

PHP needs to be a minimum version of PHP 7.4.

## Installation

### Globally (manual)

You can run these commands to easily access latest `php-cs-fixer` from anywhere on your system:

```
wget https://cs.symfony.com/download/php-cs-fixer-v3.phar -O php-cs-fixer
```

or with specified version:

```
wget https://github.com/PHP-CS-Fixer/PHP-CS-Fixer/releases/download/v3.13.0/php-cs-fixer.phar -O php-cs-fixer
```

or with curl:

```
curl -L https://cs.symfony.com/download/php-cs-fixer-v3.phar -o php-cs-fixer
```

then:

```
sudo chmod a+x php-cs-fixer
sudo mv php-cs-fixer /usr/local/bin/php-cs-fixer
```

Then, just run `php-cs-fixer`.

Place the config file `.php_cs.dist.php` in the root of your project.

## PHPStorm Configuration

1. Settings > Tools > File Watchers > Add New `Custom` Template
2. Name: `PHP CS FIXER`
3. Files to Watch:

- File type: `PHP`
- Scope: `Current file`

4. Tool to Run on Changes:

- Program: `/usr/local/bin/php-cs-fixer`
- Arguments: `fix --config=$ProjectFileDir$/.php_cs.dist.php $FileDir$/$FileName$`
