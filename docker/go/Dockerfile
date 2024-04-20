# ベースイメージを指定
FROM golang:latest

# コンテナ内の作業ディレクトリを設定
WORKDIR /app

# ローカルのソースコードをコンテナにコピー(compose.ymlのcontextを参照)
COPY ./api/app /app

# 必要なパッケージをインストール
RUN go mod download

# アプリケーションをビルド
RUN go build -o main .

# コンテナのポートを公開
EXPOSE 8080

# アプリケーションを実行
CMD ["go", "run", "main.go"]
