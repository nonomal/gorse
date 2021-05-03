# Run Gorse with Docker Compose

The best practice to manage Gorse nodes is using orchestration tools such as Docker Compose, etc.. There are Docker images of master node, server node and worker node.


| Docker Image         | Build Status |
| ------------ | -------- |
| gorse-master | [![](https://img.shields.io/docker/cloud/build/zhenghaoz/gorse-master)](https://hub.docker.com/repository/docker/zhenghaoz/gorse-master) |
| gorse-server | [![](https://img.shields.io/docker/cloud/build/zhenghaoz/gorse-server)](https://hub.docker.com/repository/docker/zhenghaoz/gorse-server) |
| gorse-worker | [![](https://img.shields.io/docker/cloud/build/zhenghaoz/gorse-worker)](https://hub.docker.com/repository/docker/zhenghaoz/gorse-worker) |

## Quick Start

There is an example [docker-compose.yml](https://github.com/zhenghaoz/gorse/blob/master/docker/docker-compose.yml) consists of a master node, a server node and a worker node, a Redis instance, and a MySQL instance.

- Setup the Gorse cluster using Docker Compose.

```bash
docker-compose up -d
```

- Download the SQL file [github.sql](https://cdn.gorse.io/example/github.sql) and import to the MySQL instance.

```
mysql -h 127.0.0.1 -u root -proot_pass gorse < github.sql
```
