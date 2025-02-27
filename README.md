# Sample Container Dotnet

このプロジェクトは、ASP.NET Coreを使用して構築されたサンプルのコンテナー化されたWebアプリケーションです。

## 必要な事前準備

1. **Docker**: Dockerがインストールされている必要があります。インストール方法については、[Dockerの公式ドキュメント](https://docs.docker.com/get-docker/)を参照してください。
2. **.NET SDK**: .NET 8.0 SDKがインストールされている必要があります。インストール方法については、[.NETの公式ドキュメント](https://dotnet.microsoft.com/download/dotnet/8.0)を参照してください。


## ビルドと実行

### Dockerを使用してビルドと実行

1. Dockerイメージをビルドします:
    ```sh
    docker build -t sample-container-dotnet -f sample-container-dotnet/Dockerfile .
    ```

2. コンテナーを実行します:
    ```sh
    docker run -d -p 8080:8080 -p 8081:8081 --name sample-container-dotnet sample-container-dotnet
    ```

### ローカル環境で実行

1. プロジェクトの依存関係を復元します:
    ```sh
    dotnet restore
    ```

2. アプリケーションをビルドします:
    ```sh
    dotnet build
    ```

3. アプリケーションを実行します:
    ```sh
    dotnet run
    ```

## アクセス

アプリケーションが実行されると、以下のURLでアクセスできます:
- HTTP: `http://localhost:8080`
- HTTPS: `https://localhost:8081`

## 設定

アプリケーションの設定は、`appsettings.json`および`appsettings.Development.json`ファイルで行います。

## ライセンス

このプロジェクトはMITライセンスの下でライセンスされています。詳細はLICENSEファイルを参照してください。