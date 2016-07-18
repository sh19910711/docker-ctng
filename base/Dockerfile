FROM ubuntu:16.04

RUN apt update
RUN apt install -y wget

RUN mkdir -p /tmp/ctng
RUN cd /tmp/ctng && wget http://crosstool-ng.org/download/crosstool-ng/crosstool-ng-1.22.0.tar.xz
RUN apt install -y xz-utils
RUN cd /tmp/ctng && tar Jxf crosstool-ng-1.22.0.tar.xz

RUN apt install -y build-essential
RUN apt install -y gperf
RUN apt install -y bison
RUN apt install -y flex
RUN apt install -y texinfo
RUN apt install -y help2man
RUN apt install -y gawk
RUN mkdir -p /tmp/libtool
RUN cd /tmp/libtool && wget http://ftpmirror.gnu.org/libtool/libtool-1.5.26.tar.gz
RUN cd /tmp/libtool && tar zxf libtool-1.5.26.tar.gz
RUN cd /tmp/libtool/libtool-1.5.26 && \
  ./configure --prefix=/usr/local && \
  make -j4 && \
  make install
RUN apt install -y automake
RUN apt install -y libncurses-dev
RUN cd /tmp/ctng/crosstool-ng && \
  ./configure --prefix=/usr/local && \
  make -j4 && \
  make install
