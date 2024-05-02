ARG BASE_IMAGE
FROM ${BASE_IMAGE}
RUN echo 'deb http://archive.debian.org/debian stretch main' >> /etc/apt/sources.list
RUN echo 'deb http://archive.debian.org/debian-security stretch/updates main' >> /etc/apt/sources.list
RUN apt-get update; apt-get install -y --no-install-recommends cron && \
    rm -r /var/lib/apt/lists/*
COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
