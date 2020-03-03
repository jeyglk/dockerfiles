FROM ubuntu:19.04
LABEL maintainer="Jeremy Mathevet <jeremy@mathevet.net>"

RUN apt-get update && apt-get install -y \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common

RUN curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add -

RUN apt-key fingerprint 0EBFCD88

RUN add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

ENTRYPOINT /usr/bin/apt-get update && /usr/bin/apt-cache madison docker-ce
