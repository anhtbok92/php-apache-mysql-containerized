ARG PHP_VERSION=""
FROM php:${PHP_VERSION:+${PHP_VERSION}-}fpm-alpine

RUN apk update; \
    apk upgrade;

RUN apk add --no-cache openssl-dev
RUN apk add --no-cache oniguruma-dev

# Install PHP extensions
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install pdo
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install openssl
RUN docker-php-ext-install mbstring
RUN docker-php-ext-install fileinfo
