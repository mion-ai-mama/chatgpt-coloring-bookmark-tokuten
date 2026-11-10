# ChatGPTで作る 塗り絵しおり 海外販売スタートガイド（特典ページ）

Instagramリール特典。静的サイト（HTML/CSS/JS・ビルドなし）。

- 文章・プロンプト・リンク: `js/content.js`（単一の源）
- 配色・余白: `css/style.css` の `:root`
- 組み立て: `js/script.js`
- ローカル確認: `python3 -m http.server 8000` → http://localhost:8000

## 画像の差し替え

「【画像差し替え予定】」の枠は、`js/content.js` の `img` に画像のパスを入れると実際の画像に切り替わります（`alt` は入っています）。

| 場所 | content.js | 推奨 |
|---|---|---|
| 3ジャンルの見本 | `cards[0]` の `gallery` の各 `img` | 横長3:2 |

画像は `assets/images/` に置きます。実在しない画面や作例は使わないでください。

## 公開手順

1. `develop` で編集 → 確認 → `main` へマージ
2. GitHub のリポジトリ（`mion-ai-mama/chatgpt-coloring-bookmark-tokuten`）を Public にし、Settings → Pages で `main` / root を選ぶ
3. 公開URL: https://mion-ai-mama.github.io/chatgpt-coloring-bookmark-tokuten/

Etsyの規約・手数料は変更されます。公開前に `js/content.js` 冒頭の `VERIFIED_DATE` と公式ページを見比べてください。
