# HT Active PHP Convention Checker by PHP CodeSniffer

## About
- **[PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)** is a set of two PHP scripts; the main phpcs script that tokenizes PHP, JavaScript and CSS files to detect violations of a defined coding standard, and a second phpcbf script to automatically correct coding standard violations. **[PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)** is an essential development tool that ensures your code remains clean and consistent.
- **[HT Active PHP Convention](https://github.com/htactive)** is a set of coding conventions used by PHP team in [HT Active Company](http://htactive.com/). It is based on the [PSR-2 Coding Style Guide](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md) with some additional rules.
- This is the Coding Standard package for Code Sniffer to check whether your codes satisfy the HT Active Convention or not.

## Install
- Install `PHP_CodeSniffer` globally by `composer`. Make sure you have `~/.composer/vendor/bin/` in your `PATH`.
```
composer global require "squizlabs/php_codesniffer=*"
```
- Move to **Standards** folder and clone this repository
```
cd ~/.composer/vendor/squizlabs/php_codesniffer/src/Standards
git clone git@github.com:htactive/coding-convention.git HTActive
```
- Check whether the HTActive Standard has been installed succesfully or not
```
phpcs -i
```
- Check your code using HTActive Convention
```
phpcs --standard=HTActive /path/to/your/code
```
- If you do not want to install this package inside **CodeSniffer Standards** folder, you can clone it to everywhere you want and specify the installed folder when you run `phpcs` command.
```
phpcs --standard=/path/to/your/coding-convention /path/to/your/code
```
- It's a pity that the default encoding used by PHP_CodeSniffer is ISO-8859-1. **Yes, it is not UTF-8**.
Therefore, you will have some problems with the words counter if you use Japanese in your codes.
You'd better change the default encoding to `UTF-8`.
```
phpcs --config-set encoding utf-8
```
Or set the encoding to `UTF-8` when running the command.
```
phpcs --standard=HTActive /path/to/your/code --encoding=utf-8
```
