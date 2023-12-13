FROM golang:1.18.8-alpine3.16 AS builder

WORKDIR /app 
COPY . .
RUN go build -o main ./index.go

FROM scratch

WORKDIR /
COPY --from=builder /app/main .
CMD ["/main"]