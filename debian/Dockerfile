FROM debian:stretch

RUN apt-get update && \  
    apt-get install -yq --no-install-recommends \
    git \
    ca-certificates \
    build-essential \
    automake \
    autoconf \
    libtool \
    gettext \
    zip \
    libpng-dev \
    mpeg2dec \
    libmpeg2-4 \
    libmpeg2-4-dev \
    libsdl2-dev \
    libopenal-dev \
    libopenal-data \
    libopenal1 \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

ARG FS_UAE_URL=https://github.com/FrodeSolheim/fs-uae.git
RUN cd /root && git clone $FS_UAE_URL

WORKDIR /root/fs-uae

CMD "/bin/bash"