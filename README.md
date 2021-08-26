#### Deploying apps with Docker Compose

https://github.com/AlexisFlach/docker-compose-exemples

Moderna applikationer är uppbyggda av flera mindre *services* som interagerar och formar en applikation. Vi kallar detta för *microsservices*.

Docker Compose är en separat CLI som installeras med Docker och används för att starta upp flera Docker containers samtidigt. En av de största fördelarna med att använda sig av Docker Compose är att vi slipper mycket onödigt arbete i Docker CLI, exempelvis networking mellan containers.

```bash
docker-compose --version
```

En docker-compose fil består av fyra styck top-level keys:

- version
- services
- networks
- volumes

**Version** är obligatorisk information och ska alltid vara på den första raden. Den definerar senaste versionen av Compose File Format (ungefär som API). Använd senaste versionen.

**Services** är var vi definerar applikationens microservices. Compose deployar dessa som sina egna containers. Services 

**Network** säger åt Docker att skapa nya nätverk.

**Volumes** är var vi berättar för Docker att skapa nya Volumes.

#### Exempel 1: visits

<img src="https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E" alt="JavaScript" style="zoom:50%;" />

<img src="https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB" alt="Express.js" style="zoom:50%;" />

```bash
Enkel webapplikation som räknar antalet besök. Varje besök lagras i en redis server.
```

