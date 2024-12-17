FROM php:7.4-apache
RUN a2enmod rewrite
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN apt-get update \
    && apt-get install -y \
        mc git \
        libzip-dev \
        zip \
#        npm \
    && docker-php-ext-install pdo pdo_mysql mysqli zip \
    && docker-php-ext-enable mysqli zip
ENV TERM xterm-256color
RUN echo PS1="'"'\[\e]0;\u@\h: \w\a\]${debian_chroot:+($debian_chroot)}\ \033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '"'" >> ~/.bashrc