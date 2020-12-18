# rayraykay/gba-poke-base
# Execute this in a directory where github.com/pret/agbcc are checked out.
FROM devkitpro/devkitarm

RUN apt-get update && \
    apt-get install -y --no-install-recommends gcc g++ make libpng-dev && \
    apt-get clean

RUN wget https://github.com/devkitPro/pacman/releases/latest/download/devkitpro-pacman.amd64.deb && \
    gdebi -n devkitpro-pacman.amd64.deb && \
    rm devkitpro-pacman.amd64.deb && \
    dkp-pacman -Scc --noconfirm

WORKDIR /agbcc
COPY ./agbcc /agbcc
RUN cd /agbcc && \
    ./build.sh

