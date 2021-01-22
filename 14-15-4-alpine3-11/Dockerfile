FROM        jrottenberg/ffmpeg:3.3.9-alpine311 AS ffmpeg

### Release Stage
FROM        node:14.15.4-alpine3.11 AS release

RUN         apk add --no-cache --update libgcc libstdc++ ca-certificates libcrypto1.1 libssl1.1 libgomp expat git

ENV         LD_LIBRARY_PATH=/usr/local/lib:/usr/local/lib64

COPY --from=ffmpeg /usr/local /usr/local
