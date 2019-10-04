FROM php:fpm
MAINTAINER Sherin Bloemendaal <info@spbsoftwareontwikkeling.nl>

RUN apt-get update && apt-get install -y zlib1g-dev libicu-dev g++ libmcrypt-dev 
RUN docker-php-ext-configure intl
RUN docker-php-ext-install intl

RUN docker-php-ext-install mbstring pdo_mysql mysqli pdo pdo_mysql 
   
ADD conf/www.conf /etc/php5/fpm/pool.d/www.conf

ENTRYPOINT php-fpm --nodaemonize

VOLUME /var/www

WORKDIR /var/www
