FROM php:8.1.1-fpm-alpine3.15

COPY --from=composer:2.1.3 /usr/bin/composer /usr/bin/composer

RUN apk add --update-cache --no-cache \
    nano && \
    docker-php-ext-install pdo_mysql

# timezoneをJSTにする
RUN apk --update-cache --no-cache add tzdata && \
    cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
    apk del --purge tzdata

COPY ./php.ini /usr/local/etc/php/php.ini

WORKDIR /home/backend
