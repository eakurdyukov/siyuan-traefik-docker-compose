# siyuan-traefik-docker-compose

Docker compose repo for SiYuan covered by Traefik reverse-proxy

SiYuan is a privacy-first personal knowledge management system, support fine-grained block-level reference and Markdown WYSIWYG.


❗ Change variables in the .env to meet your requirements.

💡 Note that the .env file should be in the same directory as docker-compose.yaml files.

Create networks for your services before deploying the configuration using the commands:

```
docker network create traefik-network
docker network create siyuan-network
```
Create directory for your data and change owner
```
chown -R 1000:1000 workspace
```
Deploy Nextcloud using Docker Compose:
```
docker compose -f 02-siyuan-docker-compose.yaml -p siyuan up -d
```
