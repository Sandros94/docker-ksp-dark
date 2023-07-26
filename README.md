# What is this?
This repo is to facilitate the deployment for [ksp dark multiplayer server](https://d-mp.org/) as a container.

Currently the main [docker-compose](./docker-compose.yml) it is for a `docker-swarm` stack deployment, using Caddy as reverse proxy (for [Filebrowser](https://filebrowser.org/)) and [Portainer](https://www.portainer.io/) as docker admin interface.

# How to use

The fastest and simplest way (untill I'll take my time to create a docker image) is to deploy that `docker-compose`, and use filebrowser to upload the unzipped content of your [downloaded DMPServer](https://d-mp.org/downloads) (make sure that the executable is at `/DMPServer/DMPServer.exe`) and simply restart the stack or the `ksp-dark` service.

## Edit the configs

Once you deployed a working DMPServer following the above, you can easily edit any configs inside the `/DMPServer/Config/` using the filebrowser's built-in editor. Remember to save and restart the DMP server to make changes take effect.

# Filebrowser

By default Filebrowser will not start, you have to manually change the replicas of it to 1 and then access it via the domain provided for Caddy reverse proxy.

Default user and password are `admin` and `admin`, remember to change them in the settings.