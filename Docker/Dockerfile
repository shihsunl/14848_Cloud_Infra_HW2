FROM ubuntu:18.04
ENV DEBIAN_FRONTEND noninteractive
MAINTAINER Shih-SungLin

# setup
RUN apt-get update
RUN apt-get install -y g++ software-properties-common build-essential language-pack-en unzip curl wget vim libpam0g-dev libssl-dev cmake cron iputils-ping
RUN add-apt-repository ppa:deadsnakes/ppa -y
RUN apt install -y python3-pip

# copy file to temp
COPY ./ /temp

WORKDIR /temp
ENTRYPOINT python3 /temp/hello.py
