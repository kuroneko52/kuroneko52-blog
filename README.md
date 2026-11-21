# kuroneko52 のブログ

Astro で構築し、Cloudflare Workers へ静的配信する個人ブログです。

## 開発

Node.js 22.12 以上が必要です。

```sh
npm install
npm run dev
```

開発サーバーは通常 `http://localhost:4321` で起動します。

## ビルドとプレビュー

```sh
npm run build
npm run preview
```

ビルド結果は `dist/` に出力されます。

## 記事の追加

Markdown または MDX 記事を `src/content/blog/` に追加します。

```md
---
title: '記事タイトル'
description: '記事の概要'
pubDate: '2026-11-20'
heroImage: '../../assets/blog-placeholder-1.jpg'
---

本文
```

## 公開設定

- 公開 URL: https://aimlessinsights.kuroneko52.workers.dev/
- Cloudflare 設定: `wrangler.toml`
- 配信ディレクトリ: `dist`

Astro のビルド後、Cloudflare Workers の静的アセットとして配信します。
