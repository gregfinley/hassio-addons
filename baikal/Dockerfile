ARG BUILD_FROM
FROM $BUILD_FROM

# Install requirements for add-on
RUN \
  apk add --no-cache \
    mariadb
RUN \ 
  apk add --no-cache \
    nginx
RUN \
  apk add --no-cache \
    php7 php7-fpm php7-opcache
RUN \
  apk add --no-cache \
    php7-gd php7-mysqli php7-zlib php7-curl

# COPY data for add-on
COPY run.sh /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]

