FROM golang:latest

ENV GOPATH /go
ENV PATH $PATH:$GOPATH/bin

RUN mkdir -p /go/src/api
COPY . /go/src/api
WORKDIR /go/src/api

RUN go get github.com/beego/bee
RUN go get github.com/astaxie/beego
RUN go get gopkg.in/mgo.v2

CMD bee run -downdoc=true -gendoc=true
