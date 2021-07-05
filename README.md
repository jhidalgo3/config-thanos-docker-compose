
# Thanos Docker Compose

Run a basic Thanos setup for local development using Docker and Docker Compose.

[Medium: Aprende a configurar Thanos usando docker-compose](https://jhidalgo3.medium.com/aprende-a-configurar-thanos-usando-docker-compose-345f6f03308a)

## Overview Thanos Installation

![Overview Thanos Installation](https://raw.githubusercontent.com/jhidalgo3/config-thanos-docker-compose/master/topology.png)

## Steps

1. Generate file configuration

```bash

$ bash script_generate_configs.sh
```

2. Run Thanos installation
```bash

$ docker-compose up
```

## Create a topology image from docker-compose

```
docker run --rm -it --name dcv -v $PWD:/input pmsipilot/docker-compose-viz render -m image --force docker-compose.yml --output-file=topology.png  --no-volumes --no-networks
```