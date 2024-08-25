# Исходники сайта [pgsql.site](https://pgsql.site)

<br/>

## Запустить локально с возможностью редактирования

Инсталлируете docker и docker-compose, далее:

```
$ cd ~
$ mkdir -p pgsql.site && cd pgsql.site
$ git clone --depth=1 https://github.com/webmakaka/pgsql.site.git .
$ docker-compose up
```

<br/>

Остается в браузере подключиться к localhost:80

<br/>

## (Устарело!)

<br/>

### Запустить pgsql.site на своем хосте с использованием docker контейнера:

```
$ docker run -i -t -p 80:80 --name pgsql.site marley/pgsql.site
```

<br/>

### Как сервис

```
$ sudo vi /etc/systemd/system/pgsql.site.service
```

вставить содержимое файла pgsql.site.service

```
$ sudo systemctl enable pgsql.site.service
$ sudo systemctl start  pgsql.site.service
$ sudo systemctl status pgsql.site.service
```

http://localhost:4006
