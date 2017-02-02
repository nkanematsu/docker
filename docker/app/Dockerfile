FROM php:7.0.15-alpine

ENV COMPOSER_ALLOW_SUPERUSER 1

RUN docker-php-ext-install pdo pdo_mysql
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer

COPY php.ini /usr/local/etc/php/conf.d/

WORKDIR /app
RUN composer install
CMD php artisan serve --host=0.0.0.0 --port=80
