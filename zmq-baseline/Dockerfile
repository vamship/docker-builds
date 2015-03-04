MAINTAINER Vamshi K Ponnapalli <vamshi.ponnapalli@gmail.com>


FROM ubuntu:14.04

# Update apt-get repositories, install dependencies for the zmq build
RUN apt-get update
RUN apt-get install -y  libtool\
                        pkg-config\
                        build-essential\
                        autoconf\
                        automake\
                        uuid-dev\
                        curl

# Download zmq sources, build, install and cleanup
RUN curl http://download.zeromq.org/zeromq-4.0.5.tar.gz -o zeromq-4.0.5.tar.gz &&\
    tar xzf zeromq-4.0.5.tar.gz &&\
    cd zeromq-4.0.5 &&\
    ./configure &&\
    make &&\
    make install &&\
    ldconfig &&\
    cd .. &&\
    rm -rf zeromq-4.0.5 &&\
    rm -f zeromq-4.0.5.tar.gz
