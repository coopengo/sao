from node:8-alpine

RUN addgroup -S -g 1306 coog && adduser -S -u 1306 -G coog coog \
    && apk add --no-cache git \
    && npm i --unsafe-perm -g grunt-cli

USER coog

COPY --chown=coog:coog sao /sao
WORKDIR /sao

COPY --chown=coog:coog ep /
ENTRYPOINT /ep
