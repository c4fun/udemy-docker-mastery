FROM wordpress:4.9.8-php5.6-apache

# Enlarge the php so it can support bigger size file
RUN mkdir -p /usr/local/etc/php/conf.d/
COPY uploads.ini /usr/local/etc/php/conf.d/uploads.ini

CMD ["apache2-foreground"]

