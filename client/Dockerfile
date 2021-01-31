FROM alpine:latest

RUN apk add --no-cache libpcap-dev git gcc g++ cmake make \
    && git clone https://github.com/spacemeowx2/switch-lan-play \
    && cd switch-lan-play && rm -rf ./server \
    && mkdir build && cd build \
    && cmake .. \
    && make \
    && mv ./src/lan-play /usr/bin/switch-lan-play \
    && chmod +x /usr/bin/switch-lan-play \
    && cd ../../ && rm -rf switch-lan-play
    
ENTRYPOINT [ "/usr/bin/switch-lan-play" ]
