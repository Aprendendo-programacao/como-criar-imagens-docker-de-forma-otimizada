FROM golang:1.7-alpine3.6 AS builder

WORKDIR /app

COPY main.go .

RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o main .

FROM alpine:3.14

WORKDIR /app

COPY --from=builder /app/main .

CMD [ "./main" ]