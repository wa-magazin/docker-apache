FROM php:7.4-apache

RUN apt-get update && apt-get install -y \
        libpng-dev libjpeg-dev libonig-dev libxml2-dev zip unzip \
    && docker-php-ext-install mysqli pdo pdo_mysql

RUN a2enmod rewrite
