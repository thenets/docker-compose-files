# Docker Swarm with Traefik 2

How to create a Swarm cluster and deploy services

## Docker Swarm cluster

```bash
# Create cluster
docker swarm init
```

## Service

```bash
export STACK_NAME=hello

# Deploy
docker stack deploy -c docker-compose.yml  ${STACK_NAME}

# Destroy
docker stack rm ${STACK_NAME}
```
