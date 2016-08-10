FROM php:7.0-fpm-alpine
# Install modules
RUN apk upgrade --update && apk add \
    autoconf file g++ gcc binutils isl libatomic libc-dev musl-dev make re2c libstdc++ libgcc libcurl binutils-libs mpc1 mpfr3 gmp libgomp \
    coreutils \
    freetype-dev \
    libjpeg-turbo-dev \
    libltdl \
    libmcrypt-dev \
    libpng-dev \
    openssl-dev \
    && docker-php-ext-install intl iconv mcrypt mysqli pdo pdo_mysql curl bcmath mbstring json opcache \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install gd 

RUN apk del autoconf file g++ gcc binutils isl libatomic libc-dev musl-dev make re2c libstdc++ libgcc libcurl binutils-libs mpc1 mpfr3 gmp libgomp \
&& rm -rf /var/cache/apk/*

CMD ["php-fpm"]