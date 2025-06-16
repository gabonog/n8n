# n8n 

Architecture:
 * Queue mode (multiple workers)
 * PostreSQL
 * Redis
 * Prepared to be behind Traefik as reverse proxy

Here you can find 2 options:
  * Local development environment with `docker-compose-devel.yaml`
  * Server deployment behind Traefik with `docker-compose-srv.yaml`. It requires an external Traefik with Docker provider configured.

## Setup

### 1. Choose your environment

Make a symlink with the correct `docker-compose` file:

  * Local: `ln -s docker-compose-devel.yaml docker-compose.yaml`
  * Server: `ln -s docker-compose-srv.yaml docker-compose.yaml`

### 2. Prepare the environment

Prepare the `.env` files:

  * `.env`. Use `.env.example` as base.
  * `db/.env`. Use `db/.env.example` as base.
  * `n8n/.env`. Use `n8n/.env.example` as base.

All the .env files follow this rules:

  * Divided by sections
  * The required ENV values, that must be manually checked/filled, are uncommented. The rest that are commented are optional.
  * All the ENV variables that have a default value, are assigned with that value.
  * If the type of the value is an Enum, it has a comment below with the possible values.

### 3. UI configuration

You can add [extra features registering the Community Edition](https://docs.n8n.io/hosting/community-edition-features/) with a License Key.

## References
 * [Official n8n GitHub Repo: n8n with PostgreSQL and Worker](https://github.com/n8n-io/n8n-hosting/tree/main/docker-compose/withPostgresAndWorker)
 * [Official nn Docs: Self-hosting n8n](https://docs.n8n.io/hosting/)
 * [Official n8n Docs: Docker Installation](https://docs.n8n.io/hosting/installation/docker/)
 * [Official n8n Docs: Server setups > Docker-Compose](https://docs.n8n.io/hosting/installation/server-setups/docker-compose/)
 * [Official n8n Docs: Community Edition features](https://docs.n8n.io/hosting/community-edition-features/)
 