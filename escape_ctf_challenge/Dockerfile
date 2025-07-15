
FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && apt install -y gcc bash sudo

RUN useradd -m ctfuser

WORKDIR /home/ctfuser

COPY escape /home/ctfuser/escape
COPY flag.txt /home/ctfuser/flag.txt

RUN chown root:root /home/ctfuser/escape && \
    chmod 4755 /home/ctfuser/escape && \
    chown root:root /home/ctfuser/flag.txt && \
    chmod 400 /home/ctfuser/flag.txt

USER ctfuser

CMD ["/bin/bash"]
