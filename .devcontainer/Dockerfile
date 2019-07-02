FROM debian:stretch-slim

ADD https://apt.puppet.com/puppet6-release-stretch.deb /puppet6-release-stretch.deb
RUN dpkg -i /puppet6-release-stretch.deb

RUN apt-get update && apt-get install pdk

RUN apt-get autoremove -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/* \
    && rm /puppet6-release-stretch.deb

ENTRYPOINT [ "pdk" ]
