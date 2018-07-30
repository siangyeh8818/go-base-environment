FROM centos:7

#RUN yum update
RUN yum -y install wget curl

RUN wget https://storage.googleapis.com/golang/go1.7.3.linux-amd64.tar.gz

RUN tar -zxf go1.7.3.linux-amd64.tar.gz -C /usr/local/

RUN mkdir /Golang

ENV GOROOT=/usr/local/go
ENV GOBIN=$GOROOT/bin
ENV GOPKG=$GOROOT/pkg/tool/linux_amd64
ENV export GOARCH=amd64
ENV GOOS=linux
ENV GOPATH=/Golang
ENV PATH=$PATH:$GOBIN:$GOPKG:$GOPATH/bin
