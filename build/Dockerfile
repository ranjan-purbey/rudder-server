FROM golang:1.16.8-alpine
RUN mkdir /app
WORKDIR /app
COPY go.mod .
COPY go.sum .
RUN go mod download
COPY . .
RUN go install
ENTRYPOINT [ "rudder-server" ]
EXPOSE 8080
