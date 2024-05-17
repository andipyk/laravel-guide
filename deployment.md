# Deployment

<!-- TOC -->

- [Deployment](#deployment)
  - [Coolify.io (Self-host/VPS)](#coolifyio-self-hostvps)
    - [Minimum Required Server](#minimum-required-server)
      - [Use case (node.js app)](#use-case-nodejs-app)
    - [Installation of Coolify.app](#installation-of-coolifyapp)
    - [Installation of Laravel](#installation-of-laravel)
      - [Requirements](#requirements)
    - [Other components](#other-components)
    - [PS (Postscript)](#ps-postscript)

<!-- /TOC -->
## Coolify.io (Self-host/VPS)

Link: <https://coolify.io/docs/resources/applications/laravel>

### Minimum Required Server

- 2 CPUs
- 2 GBs memory
- 30+ GB of storage for the images.

#### Use case (node.js app)

- 8GB of memory (average usage 3.5GB)
- 4 CPUs (average usage ~20-30%)
- 150GB disk (usage 40GB)

For the following things:

- 3 NodeJS apps
- 4 Static sites
- Plausible Analytics (for visitor analytics)
- Fider (feedback tool)
- UptimeKuma (uptime monitoring)
- Ghost (my newsletters)
- 3 Redis databases
- 2 PostgreSQL databases

### Installation of Coolify.app

1. SSH Enabled
2. Curl Installed
3. Install\
   Execute the following command on your server with **root** user.\
    ` curl -fsSL https://cdn.coollabs.io/coolify/install.sh | bash `

4. Open Coolify's UI
   \Now you can access Coolify on port `http://<ip>:8000` of your server.

### Installation of Laravel

#### Requirements

- Set `Build Pack` to `nixpacks`
- Set `APP_KEY`
- Set Ports Exposes to `80`

### Other components

```bash
DB_CONNECTION=mysql
DB_HOST=<DB_HOST>
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=

REDIS_HOST=<REDIS_HOST>
REDIS_PASSWORD=null
REDIS_PORT=6379
```

### PS (Postscript)

>Nixpacks\
To do so, you need to set the database to public. You can do so by going to your database and clicking on Accessible over the internet.\
We are working on a better solution for this.
