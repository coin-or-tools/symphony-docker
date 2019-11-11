FROM ubuntu:latest

RUN apt-get update
RUN apt-get -y install git gcc g++ gfortran make wget file pkg-config
RUN apt-get -y install libblas-dev liblapack-dev

RUN git clone https://github.com/coin-or/coinbrew /var/symphony
WORKDIR /var/symphony
RUN ./coinbrew fetch SYMPHONY --no-third-party --no-prompt
RUN ./coinbrew build SYMPHONY --no-third-party --no-prompt --prefix=/usr
