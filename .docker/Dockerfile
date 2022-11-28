FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y --no-install-recommends \
    apt-utils sudo git curl vim unzip openssh-client wget gnupg2 lsb-release software-properties-common \
    build-essential cmake \
    libopenblas-dev \
    libglib2.0-0 \
    libsm6 \
    libxext6 \
    libxrender-dev

# node.jsインストール
WORKDIR /root/
RUN curl -sL https://deb.nodesource.com/setup_14.x -o nodesource_setup.sh
COPY ./bash /root/
RUN ["/bin/bash", "/root/nodesource_setup.bash"]
RUN sudo apt install -y nodejs

# RUN sudo apt-get install -y nodejs npm

RUN sudo apt-get update && \
    sudo apt-get upgrade -y

RUN npm install express
# CMD node ./src/server.js