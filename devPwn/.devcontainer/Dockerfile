FROM ubuntu:latest

RUN apt-get update && apt-get upgrade -y

RUN apt install vim gdb python3 python3-pip file curl wget -y

RUN pip3 install pwntools --break-system-packages

WORKDIR /pwn 

RUN mkdir /pwn/.files

RUN wget https://lawcky.net/asset/pwndbg_2025.04.18_amd64.deb -o /pwn/.files/pwndbg_2025.04.18_amd64.deb

RUN apt install /pwn/.files/*.deb -y

RUN alias pwndbg="gdb"
