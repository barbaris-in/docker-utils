# docker-utils

## Installation

```
wget -O barbaris-docker-utils.tar.gz https://github.com/barbaris-in/docker-utils/archive/master.tar.gz
tar -xvf barbaris-docker-utils.tar.gz
chmod +x docker-utils-master/*
sudo mv docker-utils-master/* /usr/local/bin/

```

## Usage

Extended `docker ps` command (with IPs):
```
docker-ps
```

To collect IP addresses of started containers to /etc/hosts, use:
```
sudo docker-ips
```

To start containers from current directory and collect IP addresses of active containers to /etc/hosts, use:
```
sudo dcu
```

To stop and remove all docker containers on your system:
```
dkrclr
```


## Result

In you `/etc/hosts` you will see something like this

```
127.0.0.1       localhost

...

172.21.0.2   some_project_nginx #docker-ips
172.21.0.4   some_project_php #docker-ips
172.21.0.3   some_project_mysql #docker-ips

```

Note: There are `#docker-ips` comments in each line automatically generated
