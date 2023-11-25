### 概要
未来大2年後期授業，データベース工学の環境を作れるDockerfile.

### 使い方
1. 授業で配られた.mysqlファイルをこのリポジトリ内に入れてください．

2. Dockerfile L.17 `COPY ./ddl.sql /docker-entrypoint-initdb.d/` の.`/ddl.sql`を自分が入れたファイル名に変えてください．

3. 後は以下のコマンドを実行して下さい．
```
cd (このリポジトリ)
docker build -t mysql-ja .
docker run -d --name mysql-ja --rm -it mysql-ja
docker exec -it mysql-ja bash -c "mysql -proot"
```
