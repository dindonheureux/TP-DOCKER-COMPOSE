FROM php:8.2-fpm

# Installation des dépendances système nécessaires
RUN apt-get update && apt-get install -y \
    git \
    curl \
    zip \
    unzip \
    libzip-dev \
 && docker-php-ext-install \
    mysqli \
    pdo \
    pdo_mysql \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# Répertoire de travail
WORKDIR /var/www/html

# Exposition du port PHP-FPM
EXPOSE 9000

# Lancement de PHP-FPM
CMD ["php-fpm"]
