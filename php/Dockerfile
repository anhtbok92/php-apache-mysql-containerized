ARG PHP_VERSION=""
FROM php:${PHP_VERSION:+${PHP_VERSION}-}fpm-alpine

RUN apk update; \
    apk upgrade;

# Install necessary libraries for openssl
RUN apk add --no-cache openssl-dev

# Install PHP extensions
RUN docker-php-ext-install mysqli pdo pdo_mysql openssl

# Install mbstring
RUN docker-php-ext-install mbstring
