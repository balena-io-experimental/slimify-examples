FROM rahulthakoor/busybox-entware

# Install lighttpd
RUN opkg update &&\
    opkg install lighttpd

WORKDIR /usr/src/app

COPY src/start.sh ./

COPY src/lighttpd.conf ./

RUN mkdir -p /var/www/servers/test/pages/

COPY src/index.html /var/www/servers/test/pages/

RUN mkdir /var/tmp

CMD ["sh", "start.sh"]