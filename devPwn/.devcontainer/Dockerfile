FROM ubuntu:latest

RUN apt-get update && apt-get upgrade -y

RUN apt install vim gdb python3 python3-pip file -y

RUN pip3 install pwntools --break-system-packages

WORKDIR /pwn 

RUN mkdir /pwn/.files

COPY ./import/* /pwn/.files

RUN apt install /pwn/.files/*.deb -y

RUN alias pwndbg="gdb"
