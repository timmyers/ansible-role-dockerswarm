FROM ubuntu:17.10

RUN \
  apt-get update && \
  apt-get -y install \
    vagrant \
    python \
    python-pip && \
  rm -rf /var/lib/apt/lists/*

RUN \
  pip install \
  molecule \
  python-vagrant

RUN vagrant box add ubuntu/xenial64
