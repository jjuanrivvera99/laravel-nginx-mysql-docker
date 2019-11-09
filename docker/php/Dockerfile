FROM php:7.2-fpm-alpine

# Set working directory
WORKDIR /var/www

RUN docker-php-ext-install pdo pdo_mysql && \
    apk add bash git

# Install composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Add user for laravel application
RUN addgroup -g 1000 www
RUN adduser -S -G www -u 1000 www

# Copy helpers binaries
RUN mkdir /tmp/bin
COPY /bin/* /tmp/bin/
RUN chmod +x /tmp/bin/*
RUN mv /tmp/bin/* /bin/

# Change current user to www
USER www

# Expose port 9000 and start php-fpm server
EXPOSE 9000
CMD ["startup"]