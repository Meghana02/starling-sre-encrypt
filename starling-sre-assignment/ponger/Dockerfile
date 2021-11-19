FROM golang:1.17.3-alpine3.14

LABEL maintainer="dev <hello@starling.com>"

RUN mkdir /app
WORKDIR /app

COPY go.mod .
COPY go.sum .

RUN go mod download

COPY . .

RUN go build -o main .

EXPOSE 8080

CMD ["/app/main"]
