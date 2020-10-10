FROM alpine:3.12
LABEL maintainer="Carlos Lopes (cmplopes67@gmail.com)"

RUN apk add --no-cache bash bash-doc bash-completion
RUN apk add --no-cache clang clang-dev alpine-sdk dpkg
RUN apk add --no-cache libomp-dev

RUN ln -sf /usr/bin/clang /usr/bin/cc
RUN ln -sf /usr/bin/clang++ /usr/bin/c++

RUN update-alternatives --install /usr/bin/cc cc /usr/bin/clang 10
RUN update-alternatives --install /usr/bin/c++ c++ /usr/bin/clang++ 10
RUN update-alternatives --auto cc
RUN update-alternatives --auto c++
RUN update-alternatives --display cc
RUN update-alternatives --display c++

WORKDIR /source

CMD clang --version
