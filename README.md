# Chiba Tech ポータル リダイレクト

旧ポータルドメインへのアクセスを、新ドメインへリダイレクトする Chrome 拡張機能です。

- 旧ドメイン: `https://portal.it-chiba.ac.jp/`
- 新ドメイン: `https://portal.chibatech.ac.jp/`

パスやクエリ文字列はそのまま引き継がれます。
（例: `https://portal.it-chiba.ac.jp/login?id=1` → `https://portal.chibatech.ac.jp/login?id=1`）

## 仕組み

Manifest V3 の `declarativeNetRequest` 静的ルールを使用しています。
ページが読み込まれる前にネットワークレベルでリダイレクトするため、旧サイトの「ページが見つかりません」を経由せずに済みます

## インストール方法（未署名拡張の手動読み込み）

1. Chrome で `chrome://extensions` を開く
2. 右上の「**デベロッパーモード**」をオンにする
3. 「**パッケージ化されていない拡張機能を読み込む**」をクリック
4. このフォルダ（`manifest.json` がある階層）を選択する

これで旧ドメインにアクセスすると自動的に新ドメインへ転送されます。

## 補足
特に保守する気は何ので改変・再配布はご自由に
