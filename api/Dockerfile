FROM php:8.2-apache

# Install SQLite development dependencies
RUN apt-get update && apt-get install -y \
    libsqlite3-dev \
    && rm -rf /var/lib/apt/lists/*

# Install PDO and SQLite extensions
RUN docker-php-ext-install pdo pdo_sqlite

# Copy your application files
COPY . /var/www/html/

EXPOSE 80
