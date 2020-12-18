# rayraykay/gba-poke-builder
# Execute this using the root project directory as the context.
FROM rayraykay/gba-poke-base

WORKDIR /rom
COPY ./ /rom

RUN cd /agbcc && \
    ./install.sh ../rom && \
    cd /rom

RUN make compare
