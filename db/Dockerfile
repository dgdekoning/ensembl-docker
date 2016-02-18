FROM alpine:latest
MAINTAINER pkatsev@gmail.com

ENV LANG="en_US.UTF-8" \
    LC_ALL="en_US.UTF-8" \
    LANGUAGE="en_US.UTF-8" \
    DB_USER="admin" \
    DB_PASS="password" \
    TERM="xterm"

RUN apk -U upgrade && \
    apk --update add \
      mariadb mariadb-client \
      && \
      rm -rf /tmp/src && \
      rm -rf /var/cache/apk/*

ADD my.cnf /etc/mysql/my.cnf
ADD start.sh /sbin/start

VOLUME ["/data"]
EXPOSE 3306

CMD ["start"]
