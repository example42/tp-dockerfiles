# Dockerfile generated by tp::dockerize { 'supervisor': }
FROM debian:8
MAINTAINER Example42 GmbH <info@example42.com>

RUN apt-get update && \
    apt-get install -y --no-install-recommends supervisor && \
    rm -rf /var/lib/apt/lists/*

VOLUME /var/log/supervisor


ENTRYPOINT [ "supervisord"   , ""--nodaemon" ]
CMD [ "-c","/etc/supervisor/supervisord.conf" ]
