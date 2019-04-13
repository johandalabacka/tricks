# Xdebug on Mac OS X 10.14 with Google Chrome, Phpstorm

https://xdebug.org/docs/remote

## Install brew

## Install latest php from brew

```bash
$ brew install php
```
## Install and configure xdebug

```bash
$ pecl install xdebug
```

Cut the line from the top of /usr/local/etc/php/7.3/php.ini
```ìni
zend_extension="xdebug.so"
```

Create a file /usr/local/etc/php/7.3/conf.d/xdebug.ini. The outcommented line is
the full path.

```ini
[xdebug]
# zend_extension="/usr/local/Cellar/php/7.3.4/pecl/20180731/xdebug.so"
zend_extension="xdebug.so"
xdebug.remote_enable=1
xdebug.remote_host=127.0.0.1
xdebug.remote_port=9000
xdebug.idekey=PHPSTORM

```

Man kan oxo använda två stycken andra flaggor

callback
autostart

## Install browser extension

https://chrome.google.com/webstore/detail/xdebug-helper/eadndfjplgieldjbigjakmdgkmoaaaoc/

Right click on it and select Options (Alternativ). Change IDE key to PHPSTORM

## PHP-storm

In the Run meny select Start listening for PHP debug connections

## Visual Studio Code

Install extension 
