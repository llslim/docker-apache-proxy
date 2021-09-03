FROM php:7.4-apache

LABEL com.llslim.image.authors="info@llslim.com"

RUN set -eux; \
	if command -v a2enmod; then \
	  a2enmod rewrite deflate proxy proxy_fcgi ssl; \
	fi; 
	
#	 openssl req -x509 -nodes -days 365 -newkey rsa:2048 \
#	  -keyout /etc/ssl/private/ssl-cert-llslim.key -out /etc/ssl/certs/ssl-cert-llslim.pem \
#		 -subj "/C=US/ST=NC/L=Vien/O=Security/OU=Development/CN=localhost"


	 COPY server-name.conf /etc/apache2/conf-available/
	 COPY proxy-timeout.conf /etc/apache2/conf-available/
	 RUN a2enconf server-name

	 EXPOSE 443
	 WORKDIR /var/www/html/
