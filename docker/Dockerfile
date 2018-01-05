FROM php:7.2.0-apache

# Apache Conf
COPY docker/default.conf /etc/apache2/sites-available/000-default.conf
RUN a2enmod rewrite

# Exec
COPY docker/docker-entrypoint.sh /usr/local/bin/
RUN chmod +x /usr/local/bin/docker-entrypoint.sh
ENTRYPOINT ["docker-entrypoint.sh"]
CMD ["apache2-foreground"]
