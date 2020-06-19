# RLCraft-Server
Docker image for the Forge modded server with RLCraft installed.

Minimum starting command for online use:
```
docker run -dit -e EULA=true -p 25565:25565 doubleem/rlcraft-server
```

For saving and loading worlds and configurations attach a valume to the /server/server-data path, like so:
```
docker run -dit -e EULA=true -v rlcraft-server:/server/server-data -p 25565:25565 doubleem/rlcraft-server
```

**NOTE**: By providing EULA=TRUE you agree to the EULA at https://account.mojang.com/documents/minecraft_eula.
