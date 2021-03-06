# docker-ark 
This is docker container running an **ARK Survival Evolved** server (http://www.playark.com/).

Tested on Linux (Ubuntu 18.04)
## Features

- Easy install
- Easy to use
- Automatic backup before server update
- Work well with synology

## Requirements
- docker installed (see https://docs.docker.com/linux/)
- at least 20GB free disk space (18GB are downloaded for the game server)
- 4GB+ RAM

## Usage
- run ``docker pull alron/ark-server``
- create a folder to store the server files with enough space (i.e. /data/ark/)
- run ``docker run -d -e ARK_SERVER_NAME=serverName -e ARK_SERVER_PASSWORD=password -e ARK_SERVER_ADMIN_PASSWORD=adminPassword -e ARK_SERVER_PORT=serverPort -e ARK_SERVER_QUERYPORT=serverQueryport -e ARK_MAX_PLAYER=10 -v /data/ark:/server/ark -p 7778:7778/udp -p 27015:27015/udp alron/ark-server``

## Issues

- Server settings should be described in a GameUserSettings.ini but Synology DSM do not seem to aknowledge this file. It doesn't acknowledge some properties in the file.

