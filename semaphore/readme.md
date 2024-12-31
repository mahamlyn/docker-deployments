# Ansible Semaphore

This repository contains the docker files to build ansible semaphore, it is taken from the two following locations:

[Sempaphore Official Doco](https://docs.semaphoreui.com/administration-guide/installation/docker/)

[Chrisian Lempa - Boiler Plates](https://github.com/ChristianLempa/boilerplates/tree/main/docker-compose/ansiblesemaphore)


The passwords that are in the mysql and sempahore environments will need to be updated (this can be via an env file or within the compose file)

*remember storing passwords in compose files is not a good idea and only done for testing purposes*

The following command can be run to generate the SEMAPHORE_ACCESS_KEY_ENCRYPTION token that is required

```bash
head -c32 /dev/urandom | base64
```

The following directories need to be created to store the relevant static configuration on the system:

- inventory
- authorised-keys
- config
- semaphore-mysql
