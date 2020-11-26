FROM docker.io/richarvey/nginx-php-fpm:latest
# 修改为国内原
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories
# 安装扩展
RUN  apk update && \
        apk add --no-cache bash \
        openssh-client \
        wget \
        g++ \
        supervisor \
        curl \
        libcurl \
        git \
        python \
        python-dev \
        py-pip \
        augeas-dev \
        openssl-dev \
        ca-certificates \
        dialog \
        autoconf \
        make \
        gcc \
        musl-dev \
        linux-headers \
        libmcrypt-dev \
        libpng-dev \
        icu-dev \
        libpq \
        libxslt-dev \
        libffi-dev \
        freetype-dev \
        sqlite-dev \
        libjpeg-turbo-dev && \
        pecl install mongodb swoole && \
        rm -rf /tmp/pear && \
        docker-php-ext-enable mongodb swoole && \
        apk del gcc musl-dev linux-headers libffi-dev augeas-dev python-dev make autoconf
COPY php.ini /usr/local/etc/php/

COPY www.conf /usr/local/etc/php-fpm.d/www.conf
