# syntax=docker/dockerfile:1

FROM golang:1.19 as build

WORKDIR /src


COPY ./foo ./foo
COPY ./user ./user
COPY ./go.work ./

WORKDIR /src/user
RUN CGO_ENABLED=0 GOOS=linux go build -o /foo

CMD ["/foo"]