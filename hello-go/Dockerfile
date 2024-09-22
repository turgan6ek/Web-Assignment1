FROM golang as builder

WORKDIR /app

COPY main.go .

COPY go.mod .


RUN go build -o hello-go

#Stage 2

FROM alpine:latest

WORKDIR /app

COPY --from=builder /app/hello-go .

CMD ["./hello-go"]
 
