# laravel_enviroment
Laravelのサンプル環境

## 開発環境
- PHP ^8.0
- Laravel Framework v9.8.1
- Nginx ^1.18
- MySQL ^8.0
- Docker
- docker-compose 3.8


## Get Started


#### ローカル環境へクローンする。
```
$ cd <enviroment directory>
$ git clone https://github.com/k-iwashita-prtimes/laravel_enviroment.git
```

#### dockerをbuild, upする。
```
$ cd laravel_enviroment
$ docker compose build
$ docker compose up -d 
```

#### dockerコンテナの中で必要なセットアップを行う.
```
$ docker compose exec app bash
// コンテナの中
$ composer install
$ cp .env.example .env
$ php artisan key:generate
$ php artisan migrate
$ exit 
```

#### http://127.0.0.1:8080/ へ接続する。


#### ※MySQLに接続したい時
```
$ docker-compose exec db bash -c 'mysql -u${MYSQL_USER} -p${MYSQL_PASSWORD} ${MYSQL_DATABASE}'
```

### 更新
[ ---2022-04-16---] Laravelのバージョンを9系へアップデート
