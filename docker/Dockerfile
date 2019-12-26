FROM ubuntu:18.04
RUN sed -i.bak -e 's%http://[^ ]\+%mirror://mirrors.ubuntu.com/mirrors.txt%g' /etc/apt/sources.list
RUN apt-get update && apt-get install -y software-properties-common
RUN add-apt-repository ppa:longsleep/golang-backports
RUN apt-get update && apt-get install -y golang-go
RUN apt-get update && apt-get install -y git

WORKDIR /work

ENTRYPOINT [ "bash" ]
