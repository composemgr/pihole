## 👋 Welcome to pihole 🚀

Network-wide ad blocking via DNS sinkhole

## 📋 Description

Network-wide ad blocking via DNS sinkhole

## 🚀 Services

- **app**: pihole/pihole:latest

## 📦 Installation

### Option 1: Quick Install
```bash
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/pihole/main/docker-compose.yaml" -o compose.yml
```

### Option 2: Git Clone
```bash
git clone "https://github.com/composemgr/pihole" ~/.local/srv/docker/pihole
cd ~/.local/srv/docker/pihole
docker compose up -d
```

### Option 3: Using composemgr
```bash
composemgr install pihole
```

## 🔧 Configuration

### Environment Variables

```shell
TZ=America/New_York
APP_ADMIN_PASS=changeme_admin_password
APP_ADMIN_PASS=changeme_admin_password
```

See `docker-compose.yaml` for complete list of configurable options.

## 🌐 Access

- **Web Interface**: http://172.17.0.1:59044

## 📂 Volumes

- `./rootfs/config/pihole` - Data storage
- `./rootfs/config/dnsmasq` - Data storage

## 🔐 Security

- Change all default passwords before deploying to production
- Use strong secrets for all authentication tokens
- Configure HTTPS using a reverse proxy (nginx, traefik, caddy)
- Regularly update Docker images for security patches
- Backup your data regularly

## 🔍 Logging

```shell
docker compose logs -f app
```

## 🛠️ Management

```bash
# Start services
docker compose up -d

# Stop services
docker compose down

# Update to latest images
docker compose pull && docker compose up -d

# View logs
docker compose logs -f

# Restart services
docker compose restart
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
