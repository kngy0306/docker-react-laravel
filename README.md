# React × Laravel の環境構築

## コンテナ起動

```sh
docker-compose up -d --build
```

## Laravel

`localhost:80`にアクセスするとLaravelのウェルカムページが表示される

## React

# 開発用サーバー起動
docker-compose exec front yarn start
```

`localhost:3000`にアクセスするとReactのウェルカムページが表示される

開発用サーバーの停止は`control + c`