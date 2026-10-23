# stoneage.tokyo

Stone Age Tokyo の公式サイト。HTML と CSS だけの静的サイト（ビルド不要）。

## 構成

- `index.html`：トップ（About／Event／Interview／Release／Contact）
- `interview/index.html`：Street chain について
- `interview/kagari-mosquito.html`：Street chain の記事（Kagari Mosquito）
- `assets/style.css`：共通デザイン（色は `:root` で定義）
- `assets/img/`：画像（トップ画像 `hero.jpg`、『時代』ジャケット `jidai.jpg` を置く）
- `serve.js`：確認用サーバー（`node serve.js` → http://localhost:8634）

## 更新のしかた

- **イベントを追加**：`index.html` の `<section id="event">` 内、Archive の先頭に `<article class="event">…</article>` を1つ足す（既存のものをコピーして書き換える）
- **次回イベントの告知**：`Next Event` の `<div class="next">` の中身を書き換える
- **Street chain の回を追加**：`interview/kagari-mosquito.html` をコピーして本文を書き換え、`index.html` の Interview 欄に `sc-vol` を1つ、`interview/index.html` の一覧にカードを1つ足す（回が2つ以上になったら切り替えボタンも戻す）
- Claude Code に「○月○日のイベントを追加して」と頼めば、ここを書き換えて公開まで行える

## 公開

- GitHub Pages（main ブランチのルートを公開）
- 独自ドメイン：stoneage.tokyo
