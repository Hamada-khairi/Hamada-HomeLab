# 🏡 Hamada's Homelab - A Comprehensive Docker-Powered Infrastructure
---

## 📋 Overview

Welcome to **Hamada's Homelab**, a powerful and feature-rich environment built with Docker containers to run, manage, and monitor a wide variety of services. The homelab integrates media streaming, file sharing, DNS management, network traffic monitoring, and more—providing a self-hosted, secure, and scalable platform for both personal and experimental use.

### Key Features:
- **Automated Media Management** (Sonarr, Radarr, Jellyfin, Plex)
- **DNS & Network Control** (Bind9, AdGuard)
- **Comprehensive Monitoring & Reporting** (Zabbix, Grafana)
- **Docker Management UI** (Portainer)
- **Torrenting & Download Automation** (qBittorrent, Prowlarr)
- **Remote Access and Desktop Gateway** (Guacamole)
- **Minecraft Server Management** (Crafty)

---

## 🌐 Networks
The homelab is powered by a custom Docker network called `hamada-network` with the subnet `10.10.10.0/24`. All services are connected through this secure, internal network, ensuring isolated communication between containers.

---

## 📦 Persistent Volumes
Every important service has its data stored in Docker volumes to ensure that all configurations and data persist even after container restarts. This provides stability and security for the homelab's data.

### Volumes:
- **Grafana Data:** Stores monitoring data and dashboards.
- **Portainer Data:** Holds configurations for Docker management.
- **Bind9 Config/Cache:** Local DNS records and cache storage.
- **Plex Library:** Your media library and associated metadata.
- **AdGuard Home Sync Config:** Settings for synchronizing multiple instances of AdGuard.

---

## ⚙️ Services

### 🛠️ **Traefik** - Reverse Proxy & Load Balancer
Traefik is the backbone of the homelab's networking. It handles requests to various services and provides automatic SSL management, routing, and load balancing. 

- **Features:**
  - Dynamic routing
  - Automatic Let's Encrypt SSL support
  - HTTP to HTTPS redirection
  - Traefik Dashboard for service monitoring
  - **Access:** `https://traefik-dashboard.hamada.local`

---

### 📊 **Grafana** - Monitoring & Observability
Grafana is used to visualize time-series data and provides dashboards to monitor the health and performance of your infrastructure. It's integrated with other services like Zabbix for comprehensive monitoring.

- **Features:**
  - Custom dashboards
  - Alerts and notifications
  - Zabbix integration
  - **Access:** `https://grafana.hamada.local`

---

### 🎥 **Jellyfin & Plex** - Media Management & Streaming
Both Jellyfin and Plex are open-source media server solutions that help organize and stream your personal media library (movies, TV shows, etc.) to multiple devices within and outside the network.

- **Features:**
  - Remote media streaming (TV, Movies, Music)
  - Supports multiple users and profiles
  - Direct integration with Sonarr and Radarr for automated media organization
  - **Access Jellyfin:** `https://jellyfin.hamada.local`
  - **Access Plex:** `https://plex.hamada.local`

---

### 🎞️ **Sonarr & Radarr** - Automated Media Management
These services help automate the process of downloading and managing your media library from torrent and Usenet sources. Sonarr manages TV shows, while Radarr focuses on movies.

- **Features:**
  - Automatically downloads new episodes and movies
  - Integrates with qBittorrent for downloading
  - Fully customizable file management
  - **Access Sonarr:** `https://sonarr.hamada.local`
  - **Access Radarr:** `https://radarr.hamada.local`

---

### 🌍 **Bind9 DNS Server** - Local DNS Resolution
Bind9 acts as your private DNS server to manage and resolve DNS requests for the local network. This makes services in your homelab accessible by hostname, like `https://plex.hamada.local`.

- **Features:**
  - Fast, local DNS resolution
  - Configurable DNS records
  - Integration with AdGuard Home for DNS filtering
  - **IP:** 10.10.10.53 (Static IP)

---

### 🧲 **qBittorrent** - Torrent Client
qBittorrent is a lightweight torrent client that integrates with Sonarr, Radarr, and Prowlarr to automate media downloads. 

- **Features:**
  - Easy-to-use WebUI
  - Queue management
  - Bandwidth control and scheduling
  - **Access:** `https://qbittorrent.hamada.local`

---

### 📡 **AdGuard Home Sync** - Network-wide Ad Blocking
AdGuard provides network-wide ad blocking and privacy protection for all devices connected to your homelab's network. It blocks ads, trackers, and malicious domains.

- **Features:**
  - DNS-based ad-blocking
  - Syncs settings across multiple AdGuard instances
  - Protects the entire network from online threats
  - **Access:** `https://adguardhome-sync.hamada.local`

---

### 🖥️ **Portainer** - Docker Management UI
Portainer provides an easy-to-use web interface for managing your Docker containers, networks, and volumes. It simplifies monitoring and control of all Docker resources.

- **Features:**
  - Intuitive container management
  - Built-in logs and statistics
  - Stack deployment from templates
  - **Access:** `https://portainer.hamada.local`

---

### 🎛️ **Zabbix** - Monitoring and Metrics
Zabbix is a full-fledged monitoring platform that helps you collect and analyze metrics from various networked devices. It’s integrated with Grafana to provide real-time visualization.

- **Features:**
  - Comprehensive monitoring for servers, containers, and services
  - Customizable alerts and reports
  - Zabbix frontend and web service support
  - **Access Zabbix Server:** `https://zabbix-server.hamada.local`
  - **Access Zabbix Frontend:** `https://zabbix-frontend.hamada.local`

---

### 🖥️ **Guacamole** - Remote Desktop Gateway
Guacamole provides remote access to your desktops and servers through a web browser, supporting RDP, VNC, and SSH connections. You can manage your servers remotely without needing to install additional software on your client devices.

- **Features:**
  - Access desktops and servers from anywhere
  - Supports RDP, VNC, and SSH
  - Web-based access, no client installation required
  - **Access:** `https://guacamole.hamada.local`

---

### 🕹️ **Crafty** - Minecraft Server Manager
Crafty is a powerful web-based Minecraft server manager that allows you to control multiple Minecraft servers from a centralized interface. It's perfect for running your Minecraft server efficiently and securely.

- **Features:**
  - Real-time server monitoring
  - Player and world management
  - Easy server restarts and backups
  - **Access:** `https://crafty.hamada.local`

---

## 📚 Additional Services
- **Prowlarr**: An indexer manager that integrates with Sonarr and Radarr for tracking Usenet and torrent indexers.
  - **Access:** `https://prowlarr.hamada.local`
  
- **Transmission VPN**: A secure torrent client with integrated VPN support (disabled by default).
  
- **Requestrr**: A Discord bot for managing media requests (disabled by default).
  
---

## 🌟 Conclusion
This homelab environment is built to provide maximum functionality, security, and ease of management. Whether you're hosting your own media, automating your downloads, or monitoring your entire infrastructure, **Hamada's Homelab** has got you covered.

Each service is carefully selected and designed to work together, ensuring smooth operations, high availability, and flexibility for future expansion.

Happy Homelabbing! 🖥️🎉
