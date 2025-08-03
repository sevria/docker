# Docker

This guide walks you through running Sevria using Docker. The full configuration is defined in the `compose.yml` file.

## Overview

We use Docker Compose to orchestrate the following services:

* api – Sevria REST API built with Rust
* app – Sevria web app built using SvelteKit
* postgres – PostgreSQL database
* adminer – Web UI database manager

## Getting Started

1. Make sure Docker and Docker Compose are installed on your machine.
   You can verify this by running:

   ```bash
   docker version
   docker compose version
   ```

2. Start the stack by running:

   ```bash
   docker compose up -d
   ```

   This will pull necessary images (if not already available) and start all services in detached mode.

3. Access the services:

   * API: http://localhost:4000
   * App: http://localhost:3000
   * PostgreSQL: Available internally via `postgres:5432`
   * Adminer: http://localhost:8080

## Customization

Feel free to modify the `compose.yml` file to fit your environment. You can:

* Change exposed ports
* Mount local volumes for development
* Add environment variables (e.g., database credentials, secrets)

## Stopping the Services

To stop and remove the containers:

```bash
docker compose down
```
