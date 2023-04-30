# docker-firefox-java7-vnc

Docker container that runs an old Firefox web browser with an outdated Java plugin (1.7) and offers access to it through VNC. It can be used to support old Java code, typically found in legacy web management interfaces.

It's built on Debian Jessie. The Java support is based on OpenJDK 7 and the IcedTea plugin.

## How to build this docker image locally
Before you build, I will encourage you to change the default password on the Dockerfile for obvious reasons.

    $ docker build -t haoquanwang:firefox-java7-vnc  docker-firefox-java7-vnc

## How to start a container

    $ docker run -d --rm -p 5900:5900 --name haoquan-firefox-java7-vnc haoquanwang:firefox-java7-vnc
Now you can access Firefox with any VNC client opening localhost on standard port 5900. 
