FROM ubuntu:18.04

MAINTAINER Foo Bar (foo@bar.com)

ARG PORT=8888
ARG HTML_DIR=html

RUN \
  apt-get update && \
  apt-get install -y python python-dev python-pip python-virtualenv && \
  rm -rf /var/lib/apt/lists/* && \
  mkdir -p /srv && \
  useradd -M -s /bin/false www

USER www:www

COPY ${HTML_DIR} /srv/html

WORKDIR /srv

ENV PORT ${PORT}

EXPOSE ${PORT}/tcp

CMD cd ${HTMLDIR-html} && python -m SimpleHTTPServer ${PORT}
