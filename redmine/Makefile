
DOCKER ?= docker

# NOTE! Docker-compose gets the project name from the directory the compose file is in, 
# or the -p option, or the COMPOSE_PROJECT_NAME environmental variable. 
PROJECT_NAME=redmine

VOLUMES= \
-v $(PROJECT_NAME)_var-lib-postgresql-vol:/var/lib/postgresql \
-v $(PROJECT_NAME)_home-redmine-data-vol:/home/redmine/data

.PHONY: build push shell run start stop restart reload rm rmf release


shell:
	$(DOCKER) run --rm -i -t  $(VOLUMES) $(ENV) busybox

