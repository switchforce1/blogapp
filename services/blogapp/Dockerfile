FROM php:7.3-apache
COPY . /var/www/blogapp

RUN apt-get update && apt-get install -y git zip unzip libzip-dev

RUN apt-get update && apt-get install -y libpq-dev && docker-php-ext-install pdo pdo_pgsql

RUN docker-php-ext-install bcmath sockets zip

RUN curl -sS https://getcomposer.org/installer | php && \
    mv composer.phar /usr/local/bin/composer