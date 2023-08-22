FROM fractalnetworks/client-link-base:latest

ARG RELEASE_TAG

COPY entrypoint.sh /usr/bin/entrypoint.sh

# COPY Caddyfile.template /etc/Caddyfile.template
COPY caddy.json.template /etc/caddy.json.template

ENV NOTEWORTHY_ENV $RELEASE_TAG
ENV LINK_MTU=1380

ENTRYPOINT [ "entrypoint.sh" ]
