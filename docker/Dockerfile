FROM node:10

# Basics
RUN apt update && apt install -y --no-install-recommends make g++ curl git

# Install mwoffliner
RUN apt install -y --no-install-recommends imagemagick
RUN npm --global config set user root
RUN npm install -g mwoffliner@1.8.6
RUN apt remove -y make g++

# Boot commands
COPY .custom-bashrc /root/
CMD mwoffliner
