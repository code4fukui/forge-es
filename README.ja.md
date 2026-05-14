# forge-es


[JavaScript][] における [TLS][] （およびその他の様々な暗号化ツール）のESモジュールネイティブ実装です。

[Forge](https://github.com/digitalbazaar/forge) からフォークされました。

AES-GCM のみを変換しています（[utility](https://github.com/taisukef/AES-GCM-es)）。

## はじめに

Forge ソフトウェアは、JavaScript による [TLS][] プロトコルの完全なネイティブ実装、暗号化ユーティリティのセット、および多くのネットワークリソースを利用する Web アプリケーション開発用のツールセットです。

## パフォーマンス

Forge は高速です。他の人気のある JavaScript 暗号化ライブラリとのベンチマークは以下で確認できます：

* http://dominictarr.github.io/crypto-bench/
* http://cryptojs.altervista.org/test/simulate-threading-speed_test.html

## インストール

**注意**: パッケージングシステムやビルド済みファイルを使用する前に、[Security Considerations](#security-considerations)（セキュリティに関する考慮事項）セクションを参照してください。

Forge は [CommonJS][] モジュール構造を使用しており、ブラウザバンドル用のビルドプロセスを備えています。スタンドアロンファイルを含む古い [0.6.x][] ブランチも利用可能ですが、定期的な更新は行われません。

### Node.js

[Node.js][] で forge を使用したい場合、`npm` 経由で利用可能です：

https://npmjs.org/package/node-forge

インストール：

    npm install node-forge

その後、通常のモジュールとして forge を使用できます：

```js
var forge = require('node-forge');
```

npm パッケージには、[UMD][] 形式を使用したビルド済みの `forge.min.js`、`forge.all.min.js`、および `prime.worker.min.js` が含まれています。

### バンドル / Bower

各リリースは、[UMD][] 形式を使用したビルド済みかつ最小化された基本的な forge バンドルとして、別のリポジトリで公開されています。

https://github.com/digitalbazaar/forge-dist

このバンドルは多くの環境で使用できます。特に [Bower][] を使用してインストールすることが可能です：

    bower install forge

### jsDelivr CDN

[jsDelivr](https://www.jsdelivr.com/package/npm/node-forge) 経由で使用するには、HTML に以下を含めます：

```html
<script src="https://cdn.jsdelivr.net/npm/node-forge@0.7.0/dist/forge.min.js"></script>
```

### unpkg CDN

[unpkg](https://unpkg.com/#/) 経由で使用するには、HTML に以下を含めます：

```html
<script src="https://unpkg.com/node-forge@0.7.0/dist/forge.min.js"></script>
```

## テスト

### テスト実行の準備

    npm install

### Node.js での自動テストの実行

Forge は [Node.js][] 環境でネイティブに動作します：

    npm test

### Headless Chrome での自動テストの実行

自動テストは [Karma][] を通じて行われます。デフォルトでは Headless Chrome でテストが実行されます。

    npm run test-karma

## コントリビューション

受け入れられたすべてのコントリビューション（例：PR）は、Forge プロジェクトの他の部分で使用されているのと同じライセンスの下に置かれます。このライセンスにより、Forge は BSD License または GNU General Public License (GPL) Version 2 のいずれかの条件の下で使用することが許可されます。

参照: [LICENSE](https://github.com/digitalbazaar/forge/blob/cbebca3780658703d925b61b2caffb1d263a6c1d/LICENSE)

コントリビューションに独自のライセンスを持つサードパーティのソースコードが含まれている場合、そのライセンスが Forge のライセンスと互換性がある限り、そのライセンスを保持することができます。

[TLS]: https://en.wikipedia.org/wiki/Transport_Layer_Security
[JavaScript]: https://www.javascript.com/
[CommonJS]: http://wiki.commonjs.org/wiki/CommonJS
[0.6.x]: https://github.com/digitalbazaar/forge/tree/0.6.x
[Node.js]: https://nodejs.org/
[UMD]: https://github.com/umdjs/umd
[Bower]: http://bower.io/
[webpack]: https://webpack.js.org/
[Browserify]: http://browserify.org/
[Karma]: https://karma-runner.github.io/
