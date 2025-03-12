# R用テンプレート

## 概要

- Docker, VSCodeを用いたR環境構築用のテンプレートリポジトリ
- 使い方：「[【改訂版】開発コンテナを使ってR環境を構築！](https://yo5uke/github.io/pages/tips/241219_container/index.html)」
- `rocker/verse`イメージを使用：tidyverseパッケージ、devtools、TeX、パブリッシュ関連のパッケージはインストール済み

## Dockerfileについて

**GISを使う場合：**`FROM rocker/verse`を`FROM rocker/geospatial`に変更

**Quartoのバージョン変更：**`ENV QUARTO_MINOR_VERSION=1.6 ENV QUARTO_PATCH_VERSION=42`を任意のバージョンに変更

## ワークスペース名を変えたい場合

**`Dockerfile`:** Pythonについて、`/home/rstudio/work/.venv/`の`work`の部分を任意の名前に変える（3か所）

**`docker-compose.yml`:** `venv:/home/rstudio/work/.venv`の`work`を任意の名前に変える

**`.devcontainer/devcontainer.json`:** `"workspaceFolder": "/home/rstudio/work"`の`workを任意の名前に変える
