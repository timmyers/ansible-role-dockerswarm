FROM ubuntu:17.04

RUN \
  apt-get update && \
  apt-get -y install \
    curl

RUN \
  curl https://releases.hashicorp.com/vagrant/2.0.0/vagrant_2.0.0_x86_64.deb -o /tmp/vagrant.deb && \
  dpkg -i /tmp/vagrant.deb

RUN \
  curl -L https://vagrantcloud.com/ubuntu/boxes/xenial64/versions/20171006.0.0/providers/virtualbox.box -o /tmp/xenial.box && \
  vagrant box add ubuntu/xenial64 /tmp/xenial.box

RUN \
  apt-get -y install \
    python \
    python-pip \
    software-properties-common && \
  apt-add-repository ppa:ansible/ansible && \
  apt-get update && \
  apt-get -y install ansible && \
  rm -rf /var/lib/apt/lists/*

RUN \
  pip install \
  molecule \
  python-vagrant
