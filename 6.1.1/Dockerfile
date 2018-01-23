# From base OS image
FROM eason02/centos:7

MAINTAINER Eason Lau <eason.lau02@hotmail.com>

ENV FILEBEAT_VERSION=6.1.1

COPY ./config/filebeat.yml /

RUN curl -L -O https://artifacts.elastic.co/downloads/beats/filebeat/filebeat-${FILEBEAT_VERSION}-x86_64.rpm && \
    rpm -vi filebeat-${FILEBEAT_VERSION}-x86_64.rpm && \
    rm -f filebeat-${FILEBEAT_VERSION}-x86_64.rpm && \
    rm /etc/filebeat/filebeat.yml && \
    cp /filebeat.yml /etc/filebeat/

VOLUME /var/lib/filebeat/

CMD ["filebeat","-e"]
