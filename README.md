# ⭐ Traefik Reverse Proxy Infrastructure

This repository contains the Traefik reverse proxy configuration used in the Bounded Studios infrastructure.
It provides a simple, secure, production-ready setup for routing Docker services with automatic HTTPS via Cloudflare DNS.

---

## 📁 Repository Structure

```
docker-compose.yml     # Traefik container definition
traefik.yml            # Static Traefik configuration
.env.example           # Environment variable template
```

---

## 🚀 Features

### ✔ Automatic HTTPS (Let’s Encrypt DNS-01)
- Uses Cloudflare DNS API  
- Supports wildcard certificates  
- Works behind Cloudflare proxy  

### ✔ Static Configuration
- Clean `traefik.yml` for entrypoints, ACME, providers, dashboard  
- No long command flags inside compose  

### ✔ Dynamic Routing via Docker Labels
- Apps define routers/middlewares via labels  
- Traefik auto-discovers routes  

### ✔ Secure Dashboard Access (VPN Only)
- Dashboard bound only to WireGuard interface (e.g. `10.8.0.1:8080`)  
- Not exposed publicly  

### ✔ Secret Handling
- `.env` stores Cloudflare token + ACME email

## 🎯 What This Demonstrates

- Secure reverse proxying  
- Automatic certificate management  
- Docker-based dynamic routing  
- VPN-restricted admin access  
- Clean, production-grade configuration  
