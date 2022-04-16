# React_Laravel_MySQL_Nginx_Docker 環境

## コンテナ起動

```sh
docker-compose up -d --build
```

## Nginx

アクセスログ、エラーログはそれぞれ標準出力、標準エラー出力へのシンボリックリンク

ログ確認

```sh
docker compose logs [-f] nginx
```

## Laravel

プロジェクト作成（version 8.x）

```sh
docker-compose exec api composer create-project --prefer-dist laravel/laravel . "8.*"
```

`localhost:80`にアクセスするとLaravelのウェルカムページが表示される

## React

### 開発用サーバー起動

プロジェクト作成

```sh
docker-compose exec front npx create-react-app . --template typescript
```

```sh
docker-compose exec front yarn start
```

`localhost:3000`にアクセスするとReactのウェルカムページが表示される

開発用サーバーの停止は`control + c`

## 参考リポジトリ

https://github.com/shimotaroo/docker-nextjs-laravel-sample
