FROM ubuntu:17.10

RUN \
  apt-get update && \
  apt-get -y install \
    vagrant \
    python \
    python-pip && \
  pip install molecule && \
  rm -rf /var/lib/apt/lists/*
