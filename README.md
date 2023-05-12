# Shapes Frontend

[Shapes NFT](https://github.com/takeiyuto/shapes) のフロントエンドです。

## 前提条件

1. このレポジトリの親ディレクトリに、`blockchain` という名称で [Shapes NFT のコントラクト](https://github.com/takeiyuto/shapes-contract)のプロジェクトがあること。また、コントラクトはコンパイルされて、デプロイ済みであること。詳細は、[徹底解説 NFTの理論と実践](https://www.ohmsha.co.jp/book/9784274230608/)の第9章2節を参照してください。

2. このレポジトリの親ディレクトリに、`backend` という名称で [Shapes NFT のバックエンド](https://github.com/takeiyuto/shapes-backend)のプロジェクトがあること。また、ソースコードがコンパイル済みであること。詳細は、[徹底解説 NFTの理論と実践](https://www.ohmsha.co.jp/book/9784274230608/)の第9章3節を参照してください。

## 動作方法

1. このレポジトリをクローンし、ライブラリをダウンロードします。
```bash
git clone https://github.com/takeiyuto/shapes-frontend.git frontend
cd frontend
yarn
```

2. コントラクトの型情報を生成します。
```bash
yarn type
```

3. [index.ts](./src/index.ts) の 11 行目にある以下のような `address` 定数に、既にデプロイしてある Shapes NFT コントラクトのアドレスを記述します。
```ts
const address = "0x...CONTRACT_ADDRESS...";
```

4. webpack でコンパイルからバンドルまで行い、Web サーバを起動します。
```bash
yarn build
yarn http-server ./dist
```

5. MetaMask などのソフトウェア ウォレットが入ったブラウザで、http://127.0.0.1:8080/ を開きます。

6. ローカル Web サーバは Ctrl + C で終了できます。

## ライセンス表示

このサンプル コードは、[MIT License](LICENSE)で提供しています。

# 参照

[徹底解説 NFTの理論と実践](https://www.ohmsha.co.jp/book/9784274230608/)の第9章4節を参照してください。[本書の Web サイト](https://takeiyuto.github.io/nft-book)も参考にしてください。
