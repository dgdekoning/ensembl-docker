FROM alpine:latest
MAINTAINER Pasha Katsev <pkatsev@gmail.com>

RUN apk --update add bash rsync zlib mariadb-client && \
    rm -rf /var/cache/apk/*

RUN mkdir /data
VOLUME /data

COPY load.sh /sbin/load

CMD ["load"]
