
# ... build this image with ...
# docker build --tag=pinver/dlang:2.069.latest

FROM pinver/dlang:base

# ... first of all, always update the packages ...
RUN apt-get -q update

# ... download and install dmd ...
RUN mkdir -p /cellar/dmd && \
    curl -L http://downloads.dlang.org/releases/2.x/2.069.2/dmd.2.069.2.zip > dmd.2.069.2.zip && \
    unzip dmd.2.069.2.zip && \
    rm dmd.2.069.2.zip && \
    mv dmd2 /cellar/dmd/2.069 && \
    cp /cellar/dmd/2.069/linux/bin64/dmd /cellar/dmd/2.069/linux/bin64/dmd-2.069
ENV PATH $PATH:/cellar/dmd/2.069/linux/bin64

