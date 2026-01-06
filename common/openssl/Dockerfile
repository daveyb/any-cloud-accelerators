ARG BASEIMAGE=

FROM ${BASEIMAGE} AS build
ARG VERSION=
ARG FILENAME=openssl-${VERSION}
ARG ARCHIVE=${FILENAME}.tar.gz

RUN apt-get update && apt-get install -y -qq \
    curl \
    build-essential \
    zlib1g-dev

WORKDIR /usr/local/src
RUN curl -L -O https://github.com/openssl/openssl/releases/download/${FILENAME}/${ARCHIVE}
RUN curl -L -O https://github.com/openssl/openssl/releases/download/${FILENAME}/${ARCHIVE}.sha256
RUN sha256sum -c ${ARCHIVE}.sha256
RUN tar xzf $ARCHIVE

WORKDIR /usr/local/src/openssl-${VERSION}
RUN ./config --prefix=${OPENSSLPATH} --openssldir=${OPENSSLPATH} \
    && make \
    && make install_sw
RUN ldconfig

ENTRYPOINT ["/bin/bash"]
