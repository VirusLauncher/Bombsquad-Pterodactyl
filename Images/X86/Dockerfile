FROM        ubuntu:22.04

LABEL       author="Kris Dookharan" maintainer="krisdookharan15@gmail.com"

RUN         apt update \
    && apt-get install -y python3-pip python3.10-dev python3.10-venv libopenal-dev libsdl2-dev libvorbis-dev cmake clang-format rsync \
    && useradd -m -d /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./entrypoint.sh /entrypoint.sh
CMD         [ "/bin/bash", "/entrypoint.sh" ]