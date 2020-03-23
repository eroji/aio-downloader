This is a docker-compose that I use for my own download stack. Feel free to customize it for your own needs. I take no credit for building any of the images. You can find out more information on each of them via their respective Docker Hub pages and GitHub sources.

## DockerHub
- https://hub.docker.com/r/haugene/transmission-openvpn
- https://hub.docker.com/r/linuxserver/sabnzbd
- https://hub.docker.com/r/linuxserver/sickchill
- https://hub.docker.com/r/linuxserver/radarr
- https://hub.docker.com/r/linuxserver/jackett

## Installation
1. Pull this repo
2. Generate set of self-signed certs in config/proxy/tls as tls.crt and tls.key (Or use letsencrypt. You'll need to figure this part out as I use my own wildcard certs)
3. Edit docker-compose.yaml with your own customizations, UID/GID, shares, PIA login etc.
4. Edit config/proxy/conf.d/default.conf with your own hostnames for each of the URLs you want to resolve to each service endpoint
5. That's it. `docker-compose up -d` will bring everything up. All config will be generated into config/ directory and will persist if you need to restart containers or upgrade versions