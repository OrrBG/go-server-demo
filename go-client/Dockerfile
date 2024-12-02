# syntax=docker/dockerfile:1

FROM golang:1.23.3

# Set destination for COPY
WORKDIR /app

# Download Go modules
COPY go.mod ./
RUN go mod download

# Copy the source code. Note the slash at the end, as explained in
# https://docs.docker.com/reference/dockerfile/#copy
COPY *.go ./

ENV ServerIP="10.89.1.4"

# Build
RUN CGO_ENABLED=0 GOOS=linux go build -o /docker-gs-ping


# Run
CMD ["/docker-gs-ping"]