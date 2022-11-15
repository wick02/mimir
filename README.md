# Mimir

This is grafana's answer to prometheus long term storage. By using tenants, you can isolate and lifecycle all the metrics being saved from a prometheus server into mimir, so we can save only a few days of metrics from dev while saving a lot more in production.

## Local

This a fork of [grafana play with mimir](https://grafana.com/tutorials/play-with-grafana-mimir/) along with [minio's version](https://blog.min.io/how-to-grafana-mimir-minio-persistent-metrics-storage/)

### How to start:

* clone repo: `git clone git@github.com:wick02/mimir.git && cd mimir`
* start up: `docker compose up`

### How to access:

* Grafana: http://localhost:9000
* Mimir: http://localhost:9009 through 9016 for services (look in docker-compose.yml to see which routes to what)
* Prometheus: http://localhost:9090

### How to shutdown:

* Ctrl C to stop the compose
* `docker images -q | xargs docker rmi`
* `docker ps -qa | xargs docker rm`
* `docker volume prune` 

