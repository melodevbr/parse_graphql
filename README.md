# Batch Requesting

Nesse passo a passo vou mostrar como criar uma api com batch requesting.



## Docker e Docker-compose
Primeiro, vamos criar nosso docker compose file.

```
touch docker-compose.yml
```

Esse arquivo vai ajudar a criar a nosso ambiente.
Também vai dizer como nossos containers vão se comunicar.

### NodeJs

Pra rodar o parse precisamos de NodeJs, então vamos criar um container com NodeJs.

```
parse:
  build: ./parse
  command: ./parse/start.sh
  volumes:
    - ./parse:/usr/src/app
  ports:
    - 3000:3000
  working_dir: /usr/src/app/
```
