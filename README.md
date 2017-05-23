# consul-cluster-compose

Sometimes you just want to play with a consul cluster in containers and poke it a little.

Sets up a 7 node consul cluster with 3 servers. The only container with exposed ports is the consul instance bootstrapping the cluster. The ports it exposes by default: 8400, 8500 (web-ui) and 8600

## Requirements

docker
docker-compose

## Instructions

To run, do the following from the folder containing the docker-compose.yml
`docker-compose up -d`

## Issues

If you stop a cluster without removing all the containers, on startup, the cluster may have trouble re-electing leaders... to start from scratch you can remove all the containers with:
`docker-compose rm`
