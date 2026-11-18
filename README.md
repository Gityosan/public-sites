# public-sites

GitHub Pages で公開するサイトを、フォルダごとに並べて置くリポジトリです。ログインや認証はなく、すべて公開です。

## サイト一覧

| フォルダ | 内容 |
|---|---|
| [`rta-overlay-playground/`](./rta-overlay-playground/) | RTA配信画面 プレイグラウンド。オーバーレイの枠線・シャドウ・配置・フォントを組み替え、OBS用HTMLとして書き出せる |

ルートの `index.html` がサイト一覧のページです。サイトを追加したら、ここと `index.html` のリストに1行足してください。

## 構成

- 各サイトは `サイト名/index.html` を入口にした、ビルド不要の静的ファイルです。
- `.nojekyll` を置いているので、ファイルはそのまま配信されます（Jekyll の変換を通しません）。

## GitHub Pages の設定

1. リポジトリの **Settings → Pages** を開く
2. **Build and deployment** の Source を **Deploy from a branch** にする
3. Branch を **main**、フォルダを **/ (root)** にして保存する

数分後に `https://<ユーザー名>.github.io/public-sites/` で一覧が、`https://<ユーザー名>.github.io/public-sites/rta-overlay-playground/` でプレイグラウンドが開けます。

## rta-overlay-playground について

- 1ファイル（`index.html`）で完結しています。外部から読み込むのは Google Fonts だけです。
- 設定はブラウザの localStorage に保存されます（閲覧者ごと・端末ごと）。
- 「プレイグラウンドを丸ごと保存」で、今の設定とアップロード画像を入れた同じページを `.html` として保存できます。配信者への引き継ぎに使えます。
- 「OBS用HTMLを表示」から書き出したHTMLを、OBS のブラウザソース（1920×1080）で読み込んで使います。
