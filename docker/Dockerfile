# syntax=docker/dockerfile:1
FROM php:7.4-apache-bullseye

COPY ./var/www/html /var/www/html
COPY ./usr/local/etc/php/conf.d/xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini

# PHP 7.4だとpeclで最新のxdebugをインストールしたときにバージョン非対応になるので、2系の最後のバージョンを使う
RUN pecl install xdebug-2.9.8
# root@cad9208987b2:/var/www/html# pecl install xdebug
# pecl/xdebug requires PHP (version >= 8.0.0, version <= 8.2.99), installed version is 7.4.33
# No valid packages found
# install failed
# root@cad9208987b2:/var/www/html#
