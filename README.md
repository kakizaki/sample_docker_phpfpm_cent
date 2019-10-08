
centosイメージを使ってphp-fpmを動作させます。

## コンテナ

以下のコンテナが起動します。

* php_fpm コンテナ
  * php 7.0
* nginx コンテナ
  * nginx latest
  * localhost:80 でアクセス可能


## フォルダ構成とファイル

* nginx / nginx.conf ... nginxの設定ファイル
* nginx / conf.d / default.conf ... nginxの設定ファイル
* php / www.conf ... php-fpmの設定ファイル
* php / www.socket.conf ... php-fpmの設定ファイル (unixソケットを使用する場合)
* src / ... nginxのドキュメントルート
* temp / ... unixソケットを使用する場合の作業フォルダ
* docker-compose.yml ... コンテナ全体の設定
* Dockerfile_php ... php-fpmを動作させるDockerイメージの設定ファイル


# 使用手順

ターミナルを開き、docker-compose.yml があるディレクトリへ移動し、以下のコマンドを実行する。

```
$ docker-compose up
```

ブラウザを起動し、以下のurlへアクセスする。phpinfoの実行結果が表示されるはず。
* http://localhost/index.php




