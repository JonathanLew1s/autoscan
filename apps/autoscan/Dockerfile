FROM ghcr.io/linuxserver/baseimage-alpine:3.18

ENV \
  PATH="/app/autoscan:${PATH}" \
  AUTOSCAN_CONFIG="/config/config.yml" \
  AUTOSCAN_DATABASE="/config/autoscan.db" \
  AUTOSCAN_LOG="/config/activity.log" \
  AUTOSCAN_VERBOSITY="0"

# Binary
COPY autoscan /app/autoscan

# Add root files
COPY ["apps/autoscan/run", "/etc/services.d/autoscan/run"]

# Volume
VOLUME ["/config"]

# Port
EXPOSE 3030