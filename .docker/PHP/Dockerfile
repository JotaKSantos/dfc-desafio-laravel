FROM php:7.3.16-fpm-alpine3.11
WORKDIR /var/www

RUN apk add bash mysql-client
RUN docker-php-ext-install pdo pdo_mysql

RUN rm -rf /var/www/html

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN ln -s public html

EXPOSE 9000
ENTRYPOINT [ "php-fpm" ]
