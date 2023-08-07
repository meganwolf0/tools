FROM alpine:3.18

ARG ZARF_VER

# Install necessary tools
RUN apk add --no-cache curl sudo

# Install zarf
RUN curl -L -o zarf_v${ZARF_VER}_Linux_amd64 https://github.com/defenseunicorns/zarf/releases/download/v${ZARF_VER}/zarf_v${ZARF_VER}_Linux_amd64 && \
	chmod +x ./zarf_v${ZARF_VER}_Linux_amd64 && sudo mv ./zarf_v${ZARF_VER}_Linux_amd64 /usr/local/bin/zarf && \
	curl -L -o zarf-init-amd64-v${ZARF_VER}.tar.zst https://github.com/defenseunicorns/zarf/releases/download/v${ZARF_VER}/zarf-init-amd64-v${ZARF_VER}.tar.zst  && \
	mkdir ${HOME}/.zarf-cache && mv ./zarf-init-amd64-v${ZARF_VER}.tar.zst ${HOME}/.zarf-cache/