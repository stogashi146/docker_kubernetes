## 概要

コンテナをイメージ化する

## 手順

### 方法その 1 コンテナを commit してイメージを作成する

1. Apache コンテナを作成
   `docker run --name apa000ex22 -d -p 8092:80 httpd`

2. コンテナを作成する
   `docker commit apa000ex22 ex22_original`

3. イメージが作成されたことを確認する
   `docker image ls`

### 方法その 2 Dockerfile でイメージを作成する

1. Dockerfile を作成する

2. build コマンドを実行してイメージを作る
   'docker build -t ex22_original2 chapter6/section4/app_folder'

3. イメージが作成されていることを確認する
   `docker image ls`
