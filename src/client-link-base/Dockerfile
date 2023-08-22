FROM alpine:latest

RUN apk add gettext wireguard-tools go=1.20.7-r0 socat

RUN echo "Installing and building xcaddy" \
    && go install github.com/caddyserver/xcaddy/cmd/xcaddy@latest \
    && echo "Building caddy with plugins" \
    && cd $(go env GOPATH)/bin && ./xcaddy build v2.7.3 --with github.com/abiosoft/caddy-json-schema \
    --with github.com/mholt/caddy-l4 \
    && echo "Uninstalling GoLang" && apk del go