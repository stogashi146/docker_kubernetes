### バインドマウント

1. コンテナをバインドマウントを指定して起動
   `docker run --name apa000ex20 -d -p 8090:80 -v chapter6/section2/apa_folder:/usr/local/apache2/htdocs httpd`

2. `chapter6/section2/apa_folder/`に index.html を配置する
3. http://localhost:8090/ を開き、index.html に変わったことを確認する

### ボリュームマウント

ボリューム作成
`docker volume create apa000vol1`

ボリューム詳細情報の表示
`docker volume inspect apa000vol1`

ボリュームの削除
`docker volume rm apa000vol1`

1. ボリューム作成する
   `docker volume create apa000vol1`

2. ボリュームマウントを指定して httpd を上げる
   `docker run --name apa000ex21 -d -p 8091:80 -v apa000vol1:/usr/local/apache2/htdocs httpd`

3. ボリューム詳細情報の表示する
   `docker volume inspect apa000vol1`

   マウント先の確認
   `docker container inspect apa000ex21`
