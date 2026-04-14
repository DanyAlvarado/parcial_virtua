FROM php:8.2-apache

RUN sed -i 's/Listen 80/Listen 5572/' /etc/apache2/ports.conf

RUN apt-get update && apt-get install -y \
    libzip-dev \
    unzip \
    default-mysql-client \
    && rm -rf /var/lib/apt/lists/*

RUN docker-php-ext-install mysqli pdo pdo_mysql
RUN a2enmod rewrite

WORKDIR /var/www/html

EXPOSE 5572 

