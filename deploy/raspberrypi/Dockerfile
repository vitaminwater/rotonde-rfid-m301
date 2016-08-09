FROM resin/raspberrypi-golang:1.5

RUN apt-get update && \
    apt-get install -y libusb-1.0

RUN go get github.com/HackerLoop/rotonde && \
    go get github.com/HackerLoop/rotonde-client-go

ADD . $GOPATH/src/github.com/HackerLoop/rotonde-rfid-m301

RUN go install github.com/HackerLoop/rotonde-rfid-m301

RUN cp $GOPATH/bin/rotonde-rfid-m301 /usr/local/bin/

CMD ["/usr/local/bin/rotonde-rfid-m301"]
