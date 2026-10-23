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
- **インタビューを追加（vol.3 以降）**：
  1. `interview/dj-saboten.html` をコピーして新しいファイル名にし、本文を書き換える
  2. 全記事の `<nav class="vol-nav">` に新しい号のリンクを足す（自分の号には `aria-current="page"`）
  3. `index.html` の `vol-tabs` にボタンを1つ、その下に `card feature`（`data-vol` を揃え、`hidden` を付ける）を1つ足す
  4. `interview/index.html` の一覧にカードを足す
- Claude Code に「○月○日のイベントを追加して」と頼めば、ここを書き換えて公開まで行える

## 公開

- GitHub Pages（main ブランチのルートを公開）
- 独自ドメイン：stoneage.tokyo
