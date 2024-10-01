# Docker

## Network

```bash
docker network create go-postgres-network
```

## PostgreSQL

```bash
docker run --name go-postgres --network go-postgres-network -p 5432:5432 -e POSTGRES_DB=go -e POSTGRES_USER=admin -e POSTGRES_PASSWORD=admin -d postgres:latest
docker exec -it go-postgres
```

### URI

```bash
postgres://admin:admin@localhost:5432/go?schema=public
```
