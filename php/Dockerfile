FROM php:5-apache
RUN apt-get update && apt install -y libmemcached-dev zlib1g-dev
RUN docker-php-ext-install mysqli pdo_mysql
RUN printf "\n" | pecl install memcached-2.2.0
RUN docker-php-ext-enable memcached
ADD php.ini /usr/local/etc/php
