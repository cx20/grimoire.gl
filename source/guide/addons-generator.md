---
type: doc
title: アドオンジェネレータ
order: 2
---

Grimoire.jsのアドオンを作成するにあたっては、ジェネレータの使用が便利です。
[Yoeman](http://yeoman.io/)を利用して、作成したプロジェクトによりビルドスクリプトやバンドリングスクリプト、テスト実行環境などを自動生成します。

## インストール

Grimoire.jsのアドオンのジェネレータを用いるには、Yoemanをインストールする必要があります。
以下の手順でYoemanとアドオンのジェネレータをインストールすることが可能です。

```shell
npm i yo generator-grimoire-addons -g
```

## プロジェクトの作成

アドオンプロジェクトを作成するには、プロジェクトを作成したいディレクトリ上で以下のコマンドを実行します。

```shell
yo grimoire-addons
```

指示に従って、質問の内容を入力してください。テンプレートプロジェクトが生成されます。

## 各種コマンド

生成されたプロジェクトでは、以下のコマンドが利用可能になります。

### ビルド

```shell
npm run build
```

さらに、以下のように`-w`オプションをつけることで、`src/`フォルダ内のtsファイルが変更された際に自動でビルドが走るようにすることができます。

```shell
npm run build -- -w
```

### 開発用サーバーの起動

```shell
npm start
```

実際に作成したアドオンの動作を確認するためのサーバーを起動します。

### スキャフォールディング

**コンポーネントを生成する例**

```shell
npm run scafold -- -t component -name Test
```

これにより`src/TestComponent.ts`を生成します。

**コンバーターを生成する例**

```shell
npm run scafold -- -t converter -name Test
```

これにより`src/TestConverter.ts`を生成します。

