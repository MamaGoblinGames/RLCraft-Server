# RLCraft Server

Docker image for the Forge modded server with RLCraft installed.

## Quickstart

Minimum starting command for online use:

```shell
docker run -dit -e EULA=true -p 25565:25565 mamagoblin/rlcraft-server
```

For saving and loading worlds and configurations attach a volume to the /server/server-data path, like so:

```shell
docker run -dit -e EULA=true -v rlcraft-server:/server/server-data -p 25565:25565 mamagoblin/rlcraft-server
```

**NOTE**: By providing EULA=true you agree to the EULA at [https://account.mojang.com/documents/minecraft_eula](https://account.mojang.com/documents/minecraft_eula).

## Environment Variables

- EULA (Required)
  - Default: none
- RAM - Sets the dedicated RAM (java -Xms, -Xmx)
  - Default: 12G

## References

- JVM Parameters  
  [https://aikar.co/2018/07/02/tuning-the-jvm-g1gc-garbage-collector-flags-for-minecraft/](https://aikar.co/2018/07/02/tuning-the-jvm-g1gc-garbage-collector-flags-for-minecraft/)
- Crontab  
  [https://www.adminschoice.com/crontab-quick-reference](https://www.adminschoice.com/crontab-quick-reference)


## Building Docker Image From Source

If you download/clone this repo so that you can make adjustments to the files here, you can then run the following
docker command to build your own rlcraft docker image.

```shell
docker build -t mamagoblin/rlcraft-server .
```

## Notes

Might need optifine, but not installed yet:
https://optifine.net/adloadx?f=OptiFine_1.12.2_HD_U_G5.jar
