# Dockerfile generated by tp::dockerize { 'memcached': }
FROM alpine:3.3
MAINTAINER Example42 GmbH <info@example42.com>

RUN echo "http://dl-3.alpinelinux.org/alpine/edge/testing\nhttp://dl-3.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories
RUN apk --no-cache add memcached supervisor
RUN echo "[supervisord]\nnodaemon=true\n\n[program:memcached]\ncommand=memcached   " >> /etc/supervisord.conf

EXPOSE 11211
VOLUME  /var/log/memcached 

CMD [ "/usr/bin/supervisord" , "-c" , "/etc/supervisord.conf" ]
