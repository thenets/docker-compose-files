# Docker Swarm
STACK_NAME=hello
DOCKER_COMPOSE_FILE=docker-compose.yml

deploy:
	docker stack deploy -c $(DOCKER_COMPOSE_FILE) $(STACK_NAME)

restart:
	docker restart $$(docker ps | grep -i traefik | awk '{split($$0,a,"hello_traefik"); print "hello_traefik"a[2]}')

rm:
	docker stack rm $(STACK_NAME)
	sleep 1

debug: rm deploy
	sleep 2
	docker service logs -f hello_traefik
