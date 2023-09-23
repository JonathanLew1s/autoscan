FROM ghcr.io/linuxserver/baseimage-alpine:3.18

ENV \
  PATH="/app/autoscan:${PATH}" \
  AUTOSCAN_CONFIG="/config/config.yml" \
  AUTOSCAN_DATABASE="/config/autoscan.db" \
  AUTOSCAN_LOG="/config/activity.log" \
  AUTOSCAN_VERBOSITY="0"

# Binary
COPY autoscan /app/autoscan


RUN chown -R root:root /app && \
    chmod -R 755 /app && \
    rm -rf /tmp/*

USER abc

CMD ["/app/autoscan"]

# Volume
VOLUME ["/config"]

# Port
EXPOSE 3030