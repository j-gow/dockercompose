# Home-Server
This is a backup of my Docker compose files and any relevant notes or information pertaining to my home server.

Operating System: *Ubuntu 20.04.3 LTS*


Container management done via Portainer CE.

```
$ docker volume create portainer_data
    
$ docker run -d -p 8000:8000 -p 9443:9443 --name portainer \
    --restart=always \
    -v /var/run/docker.sock:/var/run/docker.sock \
    -v portainer_data:/data \
    cr.portainer.io/portainer/portainer-ce:2.9.3
```

Run docker compose files via terminal from respective folders.

```$ sudo docker-compose up -d```
