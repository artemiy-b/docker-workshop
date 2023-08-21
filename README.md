### Workshop Docker

Docker — программное обеспечение для автоматизации развёртывания и управления приложениями в средах с поддержкой контейнеризации, контейнеризатор приложений. Позволяет «упаковать» приложение со всем его окружением и зависимостями в контейнер, который может быть развёрнут на любой Linux-системе, а также предоставляет набор команд для управления этими контейнерами. 

Есть два основных варианта работы с Docker - cli и desktop

Для более комфортной работы с cli также желательно иметь базовые навыки работы с терминалом. Основные команды - cd, ls, pwd

Для запуска контейнера используется команда 

```docker run <название образа>```

Для примера возьмем postgres
```
docker run postgres

docker run -e POSTGRES_PASSWORD=password postgres

docker run -d -e POSTGRES_PASSWORD=password postgres

docker pull dbeaver/cloudbeaver

docker run -d -e POSTGRES_PASSWORD=password -p 5432:5432 postgres

host.docker.internal

docker run -d --rm -e POSTGRES_PASSWORD=password -p 5432:5432 postgres

docker run -d --rm -e POSTGRES_PASSWORD=password -p 5432:5432 -v C:\Users\Artemiy\Documents\pg_data:/var/lib/postgresql/data postgres

docker logs

docker run -d --rm -e POSTGRES_PASSWORD=password -p 5432:5432 -v C:\Users\Artemiy\Documents\pg_data:/var/lib/postgresql/data postgres:13



docker compose up 

-d 

down

stop

down -v    - иногда надо чистить вольюмы


docker run --rm -d -p 7010:8000 --name de-sprint-1-server-local cr.yandex/crp1r8pht0n0gl25aug1/de-sprint-1-v2:latest 

docker run -d -v /home/username/de_lessons/sprint1:/s1-lessons --rm -p 7010:8000 --name=de-sprint-1-server-local cr.yandex/crp1r8pht0n0gl25aug1/de-sprint-1-v2:latest



docker system prune

docker volume prune
docker volume prune --all
docker system prune --volumes
docker system prune --all

docker image prune -a
```