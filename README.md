# n8n in queue mode (multiple workers) PostreSQL, redis and behind Traefik

Here you can find 2 options:
  * Local development environment with `docker-compose-devel.yaml`
  * Server deployment behind Traefik with `docker-compose-srv.yaml`. It requires an external Traefik with Docker provider configured.

## Setup

First, you have to prepare the `.env` files.

  * `.env`. Use `.env.example` as base.
  * `db/.env`. Use `db/.env.example` as base.
  * `n8n/.env`. Use `n8n/.env.example` as base.

## References
 * [Official n8n GitHub Repo: n8n with PostgreSQL and Worker](https://github.com/n8n-io/n8n-hosting/tree/main/docker-compose/withPostgresAndWorker)
 * [Official nn Docs: Self-hosting n8n](https://docs.n8n.io/hosting/)
 * [Official n8n Docs: Docker Installation](https://docs.n8n.io/hosting/installation/docker/)