FROM golang:alpine
EXPOSE 8080
WORKDIR /usr/src/app
COPY . .
RUN go build

# Allow the frontend (5000) to make requests
ENV REQUEST_ORIGIN http://localhost:5000
ENV PORT 8080

CMD ["./server"]
