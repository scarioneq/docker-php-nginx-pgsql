FROM php:8.1-fpm-alpine

WORKDIR /var/www/html

COPY . .

RUN apk add --no-cache \
    libpng-dev \
    libjpeg-turbo-dev \
    libwebp-dev \
    libxml2-dev \
    postgresql-dev \
    zlib-dev \
    && docker-php-ext-configure gd --with-jpeg --with-webp \
    && docker-php-ext-install gd pdo pdo_pgsql

CMD ["php-fpm"]
