# dapr-init
Contains docker compose setup for running the Dapr side car in self-hosted mode (similar to running the `dapr init` command)

## Overview
This Docker Compose setup provides all the necessary containers for running Dapr in self-hosted mode, exactly as created by the `dapr init` CLI command.

## Containers
- **dapr_placement** - Dapr placement service (port 50005)
- **dapr_scheduler** - Dapr scheduler service (port 50006)
- **dapr_zipkin** - Zipkin for distributed tracing (port 9411)
- **dapr_redis** - Redis state store and pub/sub (port 6379)

All containers run within a dedicated `dapr-network` bridge network.

## Usage

Start all Dapr services:
```bash
docker compose up -d
```

View running containers:
```bash
docker compose ps
```

View logs:
```bash
docker compose logs -f
```

Stop all services:
```bash
docker compose down
```

## Ports
- `50005` - Placement service (gRPC)
- `58080` - Placement healthz endpoint
- `59090` - Placement metrics endpoint
- `50006` - Scheduler service (gRPC)
- `52379` - Scheduler etcd client endpoint
- `58081` - Scheduler healthz endpoint
- `59091` - Scheduler metrics endpoint
- `9411` - Zipkin UI (http://localhost:9411)
- `6379` - Redis
