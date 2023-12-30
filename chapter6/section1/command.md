## 概要

コンテナ、ホスト間でファイルをコピーする

### Section1. ホスト → コンテナにコピー

1. Apache コンテナを作成
   `docker run --name apa000ex19 -d -p 8089:80 httpd`

2. http://localhost:8089/に接続できること

3. ホストからコンテナにファイルをコピーする
   `docker cp chapter6/index.html apa000ex19:/usr/local/apache2/htdocs/`

4. http://localhost:8089/ を開き、index.html に変わったことを確認する
