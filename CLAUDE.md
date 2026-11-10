# ChatGPTで作る 塗り絵しおり 海外販売スタートガイド（特典ページ）

> 設計の共通原則は `~/.claude/CLAUDE.md` に従う。要件は `docs/requirements.md`。

## プロジェクト設定

技術スタック: HTML5 / CSS3 / Vanilla JavaScript（ビルドなし）、GitHub Pages。backend・database・環境変数なし（`.env` 系は作らない）。

## 運用ルール

- Etsyステッカー特典（chatgpt-etsy-sticker-tokuten）と同じ配色・構成（アイボリー×ブラウン＋くすみピンク）の複製。複製元と既存特典は未変更
- 文章・プロンプト・リンクの単一の源は `js/content.js`。色・余白は `css/style.css` の `:root`
- プロンプト（A/B/C・修正3つ・英語商品情報・追加テーマ）は制作指示書の文面を変更しない（英語商品情報のみ、Etsyの開示義務に合わせて項目6を追加）
- Etsyの規約・手数料・上限は公式で確認した範囲のみ記載（確認日は `VERIFIED_DATE`）。確認できないものは書かない
- CTA: ファーストビュー直下（教科書5大特典の画像）と最後の2か所。OGP画像は設定しない
- 画像は自作・本人提供のもののみ。未用意の枠は「【画像差し替え予定】」。実在しない売上・レビュー・Etsy画面を作らない
- 本番公開（GitHub Pagesへの反映）はユーザーの確認を得てから

## 命名・品質

- ファイル kebab-case / 変数 camelCase / 関数100行・ファイル700行・複雑度10・行長120以下
- ローカル確認: `python3 -m http.server <port>` を1つだけ起動

## ドキュメント管理

許可: `docs/requirements.md` / `docs/SCOPE_PROGRESS.md` / `README.md` / `LICENSE.md`。他は要許諾。

## 品質ゲート

- 第一防壁: ローカル git hook（pre-commit: 秘密情報拒否＋JS構文）
- 最終防壁: GitHub Actions `verify`（JS構文・必須ファイル・index.htmlのリンク切れ）
- ブランチ: `main`＝公開 / `develop`＝編集
