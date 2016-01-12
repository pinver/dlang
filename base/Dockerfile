
# ... build this image with ...
# docker build --tag=pinver/dlang:base.1

FROM ubuntu:15.10

# ... first af all, always update the packages ...
RUN apt-get -q update

# ... generic utilities and development tools ...
RUN apt-get -qy install \
    curl libcurl3-gnutls unzip xz-utils ssh \
    gcc g++ \
    vim

# ... download and install dub ...
RUN mkdir -p /cellar/dub/0.9.24 && \
    curl -L http://code.dlang.org/files/dub-0.9.24-linux-x86_64.tar.gz | tar xz && \
    mv dub /cellar/dub/0.9.24
ENV PATH $PATH:/cellar/dub/0.9.24

