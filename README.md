# R用テンプレート

## 概要

- Docker, VSCodeを用いたR環境構築用のテンプレートリポジトリ
- 使い方：「[【改訂版】開発コンテナを使ってR環境を構築！](https://yo5uke/github.io/pages/tips/241219_container/index.html)」
- `rocker/verse`イメージを使用：tidyverseパッケージ、devtools、TeX、パブリッシュ関連のパッケージはインストール済みの設定

## Dockerfileについて

**GISを使う場合：**`FROM rocker/verse`を`FROM rocker/geospatial`に変更

**Quartoのバージョン変更：**`ENV QUARTO_MINOR_VERSION=1.6 ENV QUARTO_PATCH_VERSION=42`を任意のバージョンに変更

## ワークスペース名の変更方法

### 1. `.devcontainer/devcontainer.json` を編集

`"workspaceFolder": "/home/rstudio/work"` の `work` を任意のフォルダ名に変更  

### 2. 開発コンテナを再起動  

**開発コンテナをまだ開いていない場合**  
- `Ctrl` + `Shift` + `P` を押して、「**コンテナーで再度開く**」を検索・実行  

**開発コンテナをすでに開いている場合**  
- `Ctrl` + `Shift` + `P` を押して、「**コンテナーのリビルド**」を検索・実行  