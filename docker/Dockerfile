FROM golang:1.19-alpine as base

WORKDIR /app

COPY . .

RUN go build -o /main main.go

FROM scratch

WORKDIR /

COPY --from=base /main /main

ENTRYPOINT [ "/main" ]