# Docker-Mini_project

# PHP + Redis Visit Counter (Docker & NFS Storage)

A containerized PHP web application that counts page visits using Redis for persistent caching. Built with multi-stage Docker builds, custom network isolation, and NFS-backed volume persistence.

## Key Features
- **Multi-Stage Build**: Keeps the runtime image lightweight by removing Composer and build dependencies from the final image.
- **NFS Network Storage**: Decouples persistent data from the host disk using an NFSv4 storage container.
- **Network Security**: Isolates Redis internally on a custom bridge subnet (`172.28.0.0/24`) without exposing port `6379` to the host.

## Tech Stack
- **Language**: PHP 8.2 (Apache)
- **Cache/Database**: Redis 7 Alpine
- **DevOps**: Docker, Docker Compose, Multi-stage Builds, NFSv4

## Quick Start

1. **Spin up the stack**:
   ```bash
   docker compose up -d --build
