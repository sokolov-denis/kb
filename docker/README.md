# Docker

## Очистка места на диске

```bash
# Удаление остановленных контейнеров
docker rm $(docker ps -a -f status=exited -q)

# Удаление неиспользуемых томов
docker volume rm $(docker volume ls -f dangling=true -q)

# Удаление неиспользуемых сетей
docker network rm $(docker network ls -f dangling=true -q)

# Удаление неиспользуемых образов
docker rmi $(docker images -f dangling=true -q)
```
