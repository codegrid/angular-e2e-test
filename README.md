angular-e2e-test
=======================

# [攻略！AngularJS](https://app.codegrid.net/series/angularjs)

[CodeGrid](http://www.codegrid.net/)の「[攻略！AngularJS | E2Eテスト](https://app.codegrid.net/entry/angularjs-12)」の記事内で使用しているサンプルです。

各サンプルの解説については上記記事をご確認ください。

## テストの実行

npmでprotractorをインストールします。

```
$ npm install -g protractor
```

Seleniumサーバーを立ち上げるために以下のコマンドを実行します。

```
$ webdriver-manager update
$ webdriver-manager start
```

このリポジトリをローカルにcloneします。

```
$ git clone https://github.com/codegrid/angular-e2e-test.git
$ cd angular-e2e-test
```

ターミナルを別タブなどで開いて`src`ディレクトリをドキュメントルートとして9000番ポートでWebサーバーを立ち上げます。

```
$ cd angular-e2e-test/src
$ python -m SimpleHTTPServer 9000
```

ターミナルをもうひとつ開いてprotractorを実行します。

```
$ cd angular-e2e-test
$ protractor conf.js
```

Chromeが立ち上がってテストが実行され、テストが通れば成功です。

## サンプルの内容

各ディレクトリの主なサンプルは以下のようものです。

### E2Eテストサンプル

- `conf.js` protractorの設定ファイル
- `tests/test.js` E2Eテストのコード
- `src/` テスト対象のアプリケーションコード
