FROM ubuntu:16.04

ENV DIR=/home/root

WORKDIR /root

RUN apt-get update && apt-get install -y \
	wget \
	git-core \
	unzip \
	mpich \
	default-jdk \
	make

RUN wget www.netlib.org/benchmark/linpackjava/LinpackJava.zip && unzip LinpackJava.zip && javac -O ~/Linpack.java

RUN git clone https://github.com/rutu-k/STREAM.git

RUN git clone https://github.com/alexandermerritt/gups.git && cd ~/gups && make -f Makefile.linux gups_vanilla

EXPOSE 80
