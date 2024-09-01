FROM caddy:2.8-builder-alpine AS caddy-builder

RUN xcaddy build --with github.com/caddy-dns/cloudflare

FROM caddy:2.8-alpine

COPY --from=caddy-builder /usr/bin/caddy /usr/bin/caddy