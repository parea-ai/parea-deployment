# Parea Deployment

Self-deploying Parea via Docker.

## Getting Started

1. Clone repository
2. Navigate into `docker` directory
3. Copy `.env.sample` to `.env` and at least fill-in `REACT_APP_SELF_HOST_ORGANIZATION_NAME`
   - required: fill-in your organization slug into `REACT_APP_SELF_HOST_ORGANIZATION_NAME`
   - optional: configure your SSO provider
   - optional: re-generate the auth/JWT secret and any secret to encrypt public keys
   - optional: update any frontend, auth or backend service ports via updating `FRONTEND_PORT`, `AUTH_PORT` or `BACKEND_PORT`
4. Run `docker-compose pull` to pull docker images
5. Run `docker-compose up -d` to start the containers 
6. Run `docker-compose down` to stop the containers

This will start:
- Parea frontend on `http://localhost:3030`
- Parea backend on `http://localhost:8000`

## Using Parea Backend in SDK

To use the self-deployed Parea backend in the SDK, you need to set the `PAREA_BASE_URL` environment variable to the backend URL.

## Updating Parea Deployment

1. Run `docker-compose pull` to pull images
2. Run `docker-compose down` to stop the containers
3. Run `docker-compose up -d` to start the containers