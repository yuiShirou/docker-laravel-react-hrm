FROM php:8.0-fpm

# Install dependencies
RUN apt-get update && apt-get install -y \
    git \
    curl \
    libpng-dev \
    libjpeg-dev \
    libfreetype6-dev \
    zip \
    unzip

# Install PHP extensions
RUN docker-php-ext-install pdo_mysql gd

# Install Composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# Set working directory
WORKDIR /var/www/html

# Copy Laravel code to container
COPY . .

# Install Laravel dependencies
RUN composer install

# Set permissions for Laravel
RUN chown -R www-data:www-data /var/www/html/storage /var/www/html/bootstrap/cache

EXPOSE 80

CMD ["php-fpm"]
