### docker 速習会

+ docker-toolbox install 確認

```
docker -v
>Docker version 1.8.1, build d12ea79

docker-machine -v
>docker-machine version 0.4.1 (e2c88d6)

docker-compose -v
>docker-compose version: 1.4.0
```

#### docker の基本

+ docker コンテナとイメージ

> imageがあってそれをもとにコンテナが作れる
１つのイメージから複数のコンテナを作成可能

+ docker デーモン

> APIリクエストを送るとコンテナを作る
プロセスがある
コマンドラインインターフェースがdocker デーモンのラッパー
dockderデーモンはLinuxの機能に依存してるので Mac などでは動かない

+ APIクライアント

> dockder run hogehoge
みたいなやつ

+ docder レジストリ

+ コンテナを動かす

```
dockder run <オプション> hogehoge
```

```dockder.ex
docker run \
> -d \  # バックグラウンドで起動
> -p 80:4567 \  # port 80 で 4567と紐付けて起動
> --name hello \ 
> spesnova/hello-world \
> bundle exec ruby app.rb
```
+ delete 

```
docker stop hello && docker rm hello
```

+ log 

```
dockder logs -f hogehoge # -f で tail -f みたいな
```

+ docker compose

>dockder-compose.yml を定義できる
糞長い docker run コマンドを ymlで定義できる

