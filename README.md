# hator

***

## Docker

Start service:

    docker-compose up -d

Scale up:

    docker-compose scale tor=20

## Test IP

    curl --socks5 localhost:9050 api.ipify.org
