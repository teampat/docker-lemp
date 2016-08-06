FROM php:7.0-fpm
# Install modules
RUN apt-get update && apt-get install -y libmcrypt-dev libicu-dev libpng12-dev libjpeg-dev libcurl4-gnutls-dev libxml2-dev libssl-dev \
	&& rm -rf /var/lib/apt/lists/* \
	&& docker-php-ext-install intl \
	&& docker-php-ext-install mysqli \
	&& docker-php-ext-install pdo \
	&& docker-php-ext-install pdo_mysql \
	&& docker-php-ext-install iconv \
	&& docker-php-ext-install mcrypt \
	&& docker-php-ext-install opcache \
	&& docker-php-ext-install mbstring \
	&& docker-php-ext-install gd \  
	&& docker-php-ext-install curl \ 
	&& docker-php-ext-install xml \ 
	&& docker-php-ext-install json

CMD ["php-fpm"]