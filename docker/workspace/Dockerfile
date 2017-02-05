FROM php:7.0.15-alpine

ENV COMPOSER_ALLOW_SUPERUSER 1
RUN docker-php-ext-install pdo pdo_mysql
COPY php.ini /usr/local/etc/php/conf.d/
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer
