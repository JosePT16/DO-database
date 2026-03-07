# Database

PostgreSQL schema and seed data for the e-commerce demo.

## Contents
- `init.sql` creates tables and inserts sample products.

## Local Usage (Postgres)
```bash
psql -U postgres -d ecommerce -f init.sql
```

## Docker Compose (All Services)
This repo contains a `docker-compose.yml` that builds and runs all services.

```bash
docker compose up --build
```

## Container Security Scan
```powershell
./scripts/scan.ps1 -ImageTag do-database:local
```

## Development Workflow (Git Flow)
1. Create a feature branch from `develop`: `feature/<name>`
2. Commit changes on the feature branch
3. Open a PR into `develop`
4. Create a release branch from `develop`: `release/<version>`
5. Merge `release/<version>` into `main` and tag the release
6. Merge `main` back into `develop`
7. For urgent fixes, create `hotfix/<version>` from `main`, then merge into `main` and `develop`
