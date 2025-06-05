FROM golang:1.23

WORKDIR /app

COPY go.mod go.sum ./
RUN go mod download
COPY *.go ./

RUN GOOS=linux GOARCH=amd64 go build -o golang-demo
RUN chmod +x golang-demo

EXPOSE 8080

CMD ["./golang-demo"]
