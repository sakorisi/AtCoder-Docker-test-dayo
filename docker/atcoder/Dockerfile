FROM ubuntu:latest

ARG DEBIAN_FRONTEND=noninteractive

ENV TZ=Asia/Tokyo

WORKDIR /app

RUN apt-get update && \
    apt-get install -y \
    time \
    tzdata \
    tree \
    git \
    curl \
    gcc-9 \
    g++-9 \
    gdb \
    python3.10 \
    pypy3 \
    python3-pip 

RUN update-alternatives --install /usr/bin/pip pip /usr/bin/pip3 10 && \
    update-alternatives --install /usr/bin/python python /usr/bin/python3.10 10 && \
    update-alternatives --install /usr/bin/pypy pypy /usr/bin/pypy3 10

RUN pip install -U pip && \
    pip install numpy scipy scikit-learn numba networkx

RUN git clone https://github.com/atcoder/ac-library.git /lib/ac-library 
ENV CPLUS_INCLUDE_PATH /lib/ac-library
