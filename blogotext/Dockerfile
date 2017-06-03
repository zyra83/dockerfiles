FROM php:7.0-apache
MAINTAINER Mickaël Benoit <zyra83@hotmail.com>

ENV RELEASE jessie
ENV DEBIAN_FRONTEND noninteractive
ENV SHELL /bin/bash


RUN apt-get update

RUN apt-get install -y --no-install-recommends unzip git ca-certificates curl

RUN curl -R -L -O http://lehollandaisvolant.net/blogotext/blogotext.zip \
    && unzip blogotext.zip -d /tmp \
	&& rm -rf /var/www/html \
	&& mv /tmp/blogotext /var/www/html \
	&& chmod 777 -R /var/www/html

EXPOSE 80


