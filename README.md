# Parea Deployment

Self-deploying Parea via Docker.

## Getting Started

1. Clone repository
2. Navigate into `docker` directory
3. Copy `.env.sample` to `.env` and fill in the necessary encryption keys
4. Copy `.env.backend.local.sample` to `.env.backend.local` and fill in the necessary encryption keys
5. Copy `.env.frontend.local.sample` to `.env.frontend.local` and fill in the necessary values
6. Copy `.env.frontend.auth.sample` to `.env.auth.local` and fill in the values to enable SSO provider(s)
7. Run `docker-compose pull` to pull images
8. Run `docker-compose up -d` to start the containers
9. Run `docker-compose down` to stop the containers

## Updating Parea

1. Run `docker-compose pull` to pull images
2. Run `docker-compose down` to stop the containers
3. Run `docker-compose up -d` to start the containers