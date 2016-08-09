FROM resin/raspberrypi-golang:1.5

RUN apt-get update && \
    apt-get install -y libusb-1.0

RUN go get github.com/HackerLoop/rotonde && \
    go get github.com/HackerLoop/rotonde-client-go

RUN go get github.com/HackerLoop/rotonde-rfid-m301 && \
    go install github.com/HackerLoop/rotonde-rfid-m301 && \
    mv /go/bin/rotonde-rfid-m301 /usr/local/bin/

CMD ["/usr/local/bin/rotonde-rfid-m301"]
