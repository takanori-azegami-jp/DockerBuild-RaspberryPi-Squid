# docker-rpi-squid
RaspberryPi(64bit)にDockerでSquidプロキシーサーバを構築

## 環境
- kernel：Linux ホスト名 5.15.32-v8+ #1538 SMP PREEMPT Thu Mar 31 19:40:39 BST 2022 aarch64 GNU/Linux
- OS：Debian GNU/Linux 11 (bullseye)

## Dockerコマンド
```bash
# Docker-compose実行
$ docker-compose up -d

# Docker コンテナ確認
$ docker ps

# Docker イメージ確認
$ docker images

# Docker コンテナの中に入る
$ docker exec -it [コンテナID] /bin/sh

# dokcer-composeのリビルド
$ docker-compose up -d --build  --force-recreate

# dokcer-composeの一括削除（滅びの呪文）
$ docker-compose down --rmi all --volumes --remove-orphans
```

## ブラウザからアクセスして動作確認
```js
http://[ホストPCのipアドレス]:3128
※存在しないURLなので「ERROR」が表示されるが動作としては正常
```
![picture 1](images/README/1670203178388.png)  

## 参考サイト
- [アプリケーションのHTTPプロキシのテスト環境を作る](https://qiita.com/megmogmog1965/items/9101a6c91bdce6d43aa4)
- [Squid で安全なインターネットアクセス環境を構築する方法](https://blog.cybozu.io/entry/2017/02/03/080000)
