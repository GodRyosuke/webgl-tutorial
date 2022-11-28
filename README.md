# dockerを用いたnode jsの実行環境
webGLを実行するため，node jsを使って実行環境を構築した．

## 実行環境
Windows10 64bit

## System requirements
Docker

## build
```bash
git clone https://github.com/GodRyosuke/webgl-tutorial.git
cd .docker
docker build -t node-js:base .
```

## Usage
```bash
docker compose up -d
docker compose exec webgl bash
cd src
node server.js
```
ウェブブラウザでlocalhost:3000にアクセスすると，サンプルプログラムがみられる．

## 参考文献
https://github.com/invent-box/Learn-WebGL
