# golden-edge-router

This repository contains the necessary files to run a golden-edge router, which consists of 
a `zenohd` container communicating with an `influxdb` container (the historian).

This requires a `.env` file with the following entries:
```
// only needed for running the router outside of a container environment
INFLUXDB_ADMIN_USERNAME="..."
INFLUXDB_ADMIN_PASSWORD="..."

DOCKER_INFLUXDB_INIT_MODE="setup"
DOCKER_INFLUXDB_INIT_USERNAME="..."
DOCKER_INFLUXDB_INIT_PASSWORD="..."
DOCKER_INFLUXDB_INIT_ORG="ielabs"
DOCKER_INFLUXDB_INIT_BUCKET="meta"
DOCKER_INFLUXDB_TOKEN="..."
```
See [influxdb documentation](https://github.com/docker-library/docs/blob/master/influxdb/README.md) for more information on the `.env` file.