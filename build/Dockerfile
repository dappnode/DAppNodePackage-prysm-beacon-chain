FROM ubuntu as binary

ARG VERSION
ENV DOWNLOAD_URL https://github.com/prysmaticlabs/prysm/releases/download
ENV BINARY_URL $DOWNLOAD_URL/$VERSION/beacon-chain-$VERSION-linux-amd64

RUN apt update && \
    apt install -y wget && \
    wget $BINARY_URL -O /usr/local/bin/beacon-chain && \
    chmod +x /usr/local/bin/beacon-chain

FROM ubuntu

#Copy binaries from build stage
COPY --from=binary /usr/local/bin/beacon-chain /usr/local/bin/beacon-chain

RUN apt update && \
    apt install -y ca-certificates && \
    rm -rf /var/lib/apt/lists/*

ADD ssl /ssl/


ENTRYPOINT [ "sh", "-c", "exec beacon-chain --datadir=/data --log-file=/data/beacon-chain.log --rpc-host 0.0.0.0 --grpc-gateway-host 0.0.0.0 --monitoring-host 0.0.0.0 --http-web3provider=$HTTP_WEB3PROVIDER $EXTRA_OPTS" ]