# Minecraft Fabric Server

Built using https://docker-minecraft-server.readthedocs.io/

## Prerequisities

- Docker
- Docker Compose

## Install

1. Copy `.env.example` as `.env`
2. Deploy using `docker-compose up -d`

## Configure

- `server.properties`
- JVM options

Add any variables from [documentation](https://docker-minecraft-server.readthedocs.io/en/latest/variables/) added to `.env` will be used next time you deploy.

## Mods

Copy mods to `data/mods` folder and deploy.

## World

Copy world to `data/world` folder.

By default, world is loaded from `data/$LEVEL` folder.

You can change this variable in `.env`.

## `data` folder

Anything copied to `data` folder will be copied to server root and available by server runtime.

## Sending commands

As described in [documentation](https://docker-minecraft-server.readthedocs.io/en/latest/commands/), use RCON.

Example:

```
# rcon-cli
> auth setGlobalPassword New-Password4
```

Tip: you cannot use `#` character in global password. Maybe other special characters is not working too.
