# stoneage.tokyo

Stone Age Tokyo の公式サイト。HTML と CSS だけの静的サイト（ビルド不要）。

## 構成

- `index.html`：トップ（About／Event／Interview／Release／Contact）
- `interview/index.html`：「路像」について
- `interview/dj-saboten.html`：インタビュー記事
- `assets/style.css`：共通デザイン（色は `:root` で定義）
- `assets/img/`：画像（トップ画像 `hero.jpg`、『時代』ジャケット `jidai.jpg` を置く）
- `serve.js`：確認用サーバー（`node serve.js` → http://localhost:8634）

## 更新のしかた

- **イベントを追加**：`index.html` の `<section id="event">` 内、Archive の先頭に `<article class="event">…</article>` を1つ足す（既存のものをコピーして書き換える）
- **次回イベントの告知**：`Next Event` の `<div class="next">` の中身を書き換える
- **インタビューを追加**：`interview/dj-saboten.html` をコピーして新しいファイル名にし、トップと `interview/index.html` にカードを足す
- Claude Code に「○月○日のイベントを追加して」と頼めば、ここを書き換えて公開まで行える

## 公開（予定）

- ホスティング：Cloudflare Pages または GitHub Pages（無料枠）
- ドメイン：stoneage.tokyo（お名前.com、本人名義）。DNS を新しいホスティングに向ける
- `@stoneage.tokyo` のメールは使っていない（MX レコードの心配なし）
- 問い合わせ先：stone.age.since2018@gmail.com
- 切り替えは花王財団の締切（2026-11-10）の後。新サイトの表示を確認してから DNS を切り替え、STUDIO 側の独自ドメイン設定は最後に外す
