FROM docker.io/richarvey/nginx-php-fpm:latest

COPY php.ini /usr/local/etc/php/
COPY www.conf /usr/local/etc/php-fpm.d/www.conf
#安装redis
#RUN set -xe \
#    && apk add --no-cache --update --virtual .phpize-deps $PHPIZE_DEPS \
#    && pecl install -o -f redis  \
#    && echo "extension=redis.so" > /usr/local/etc/php/conf.d/redis.ini \
#    && rm -rf /usr/share/php \
#    && rm -rf /tmp/* \
#    && apk del  .phpize-deps
