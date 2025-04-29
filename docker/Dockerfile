FROM php:8.2-apache

RUN apt-get update && apt-get install -y \
        libpng-dev libjpeg-dev libonig-dev libxml2-dev zip unzip \
        libzip-dev libfreetype6-dev libwebp-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp \
    && docker-php-ext-install -j$(nproc) gd mysqli pdo pdo_mysql mbstring exif zip

RUN a2enmod rewrite