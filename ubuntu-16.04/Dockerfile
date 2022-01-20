FROM ubuntu:16.04

RUN apt-get update \
  && apt-get install -y --no-install-recommends locales \
     wget rsyslog systemd systemd-cron sudo iproute2\
  && rm -Rf /var/lib/apt/lists/* \
  && rm -Rf /usr/share/doc && rm -Rf /usr/share/man \
  && apt-get clean

RUN sed -i 's/^\($ModLoad imklog\)/#\1/' /etc/rsyslog.conf

CMD ["/lib/systemd/systemd"]
