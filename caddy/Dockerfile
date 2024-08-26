FROM caddy:builder-alpine AS builder
RUN xcaddy build \
  --with github.com/caddy-dns/cloudflare \
  --with github.com/caddyserver/replace-response \
  --with github.com/caddyserver/transform-encoder

FROM caddy:alpine as runtime

RUN chown -R 1000:1000 /config/caddy
RUN chown -R 1000:1000 /data/caddy

COPY --from=builder /usr/bin/caddy /usr/bin/caddy
