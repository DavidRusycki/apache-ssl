FROM php:8.2-apache

RUN a2enmod ssl && a2enmod rewrite
RUN mkdir -p /etc/apache2/ssl
RUN mv "$PHP_INI_DIR/php.ini-development" "$PHP_INI_DIR/php.ini"

COPY ./certificado/* /etc/apache2/ssl/
COPY ./configuracao/000-default.conf /etc/apache2/sites-available/000-default.conf

EXPOSE 80
EXPOSE 443