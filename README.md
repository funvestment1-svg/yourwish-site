# yourwish-site

Petit Works Apps の公開用最小サイト。Google Play Console 組織アカウント確認（Google Search Console 経由の所有権確認）のために GitHub Pages で公開しています。

## 公開URL

`https://funvestment1-svg.github.io/yourwish-site/`

GitHub Pages の有効化: Settings > Pages > Source を「Deploy from a branch」、Branch を `main` / `(root)` に設定してください。

## Search Console 所有権確認

### サブドメイン（github.io）のまま運用する場合

URLプレフィックスタイプで登録し、発行された `google-site-verification` の値を [index.html](index.html) の `<head>` 内、コメントアウトされている `<meta name="google-site-verification" ...>` タグに追記してコメントを外してください。

### 独自ドメインを使う場合

ドメインプロパティ + DNS TXTレコードで確認するため、コード側の対応は不要です。ドメインを使う場合は以下の手順でこのリポジトリを設定してください。

1. リポジトリ直下に `CNAME` ファイルを追加し、中身を取得したドメイン1行のみにする（例: `example.com`）
2. DNS設定
   - `www` サブドメイン用 CNAME レコード: `funvestment1-svg.github.io`
   - ルートドメイン用 Aレコード（4件すべて追加）:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
3. GitHub の Settings > Pages で Custom domain にドメインを登録し、DNS反映後に Enforce HTTPS を有効化する
