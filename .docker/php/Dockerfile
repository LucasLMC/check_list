FROM php:8.1.0-fpm

# Install Mysql PDO
RUN docker-php-ext-install pdo pdo_mysql

# Update system
RUN apt-get update

# Installing tools
RUN apt-get -y install apt-utils nano vim wget 

# Installing libraries
RUN apt-get -y install --fix-missing \
    apt-utils \
    build-essential \
    curl \
    git \
    libcurl4 \
    libcurl4-openssl-dev \
    libzip-dev \
    libbz2-dev \
    libmcrypt-dev \
    libicu-dev \
    libonig-dev \
    libxml2-dev \
    locales \
    zip \
    zlib1g-dev 

RUN docker-php-ext-install \
    exif \ 
    pcntl \
    bcmath \
    curl \
    ctype \
    iconv \
    xml \
    soap \
    pcntl \
    mbstring \
    bz2 \
    zip \
    intl

# Installing Postgres PDO
RUN apt-get install -y libpq-dev \
    && docker-php-ext-configure pgsql -with-pgsql=/usr/local/pgsql \
    && docker-php-ext-install pdo pdo_pgsql pgsql