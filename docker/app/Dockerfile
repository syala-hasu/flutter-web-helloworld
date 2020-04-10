FROM ubuntu:18.04

LABEL maintainer "Ekahs"

RUN apt-get update \
      && apt-get install -y \
      git \
      curl \
      wget \
      unzip 

WORKDIR /root

RUN git clone https://github.com/flutter/flutter.git -b stable

ENV PATH $PATH:/root/flutter/bin

RUN flutter channel dev

RUN flutter upgrade

RUN flutter config --enable-web

RUN flutter doctor

WORKDIR /root/workspace/app
