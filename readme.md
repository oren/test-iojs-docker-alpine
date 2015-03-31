# Run io.js tests on Docker based on Alpine Linux

## Prerequisites

* [Docker](https://docs.docker.com/installation)
* [Compose](https://docs.docker.com/compose/install)

## Build io.js and run tests

    wget https://iojs.org/dist/v1.6.2/iojs-v1.6.2.tar.xz
    xz -cd iojs-v1.6.2.tar.xz | tar -xvf -
    cd iojs-v1.6.2
    docker-compose build
    docker-compose run web sh
    cd /tmp/iojs-v1.6.2
    ./configure --prefix=/usr --shared-openssl --shared-zlib
    make
    make test
