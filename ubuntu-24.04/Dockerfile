FROM ubuntu:24.04

RUN apt update -y && \
  apt install -y nftables && \
  apt clean && rm -rf /var/lib/{apt,dpkg,cache,log}/

COPY nftables.conf /etc/nftables.conf

VOLUME ["/etc/nftables"]

CMD ["nft", "-f", "/etc/nftables.conf"]
