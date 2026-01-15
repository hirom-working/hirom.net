# CLAUDE.md - hirom.net

Astroベースの個人ブログプロジェクト固有のガイダンスです。

## プロジェクト概要

- **フレームワーク**: Astro 5.x（astro-chiriテーマベース）
- **言語**: TypeScript
- **パッケージマネージャー**: pnpm
- **デプロイ先**: Netlify

## 主要コマンド

| タスク | コマンド | 説明 |
|--------|---------|------|
| 開発サーバー起動 | `pnpm dev` | ローカル開発サーバー |
| ビルド | `pnpm build` | 本番用静的サイト生成 |
| プレビュー | `pnpm preview` | ビルド結果のプレビュー |
| リント | `pnpm lint` | ESLintチェック |
| リント修正 | `pnpm lint:fix` | ESLintエラー自動修正 |
| フォーマット | `pnpm format` | Prettier整形 |
| 新規記事作成 | `pnpm new` | 対話式で新規記事作成 |

## コンテンツ管理

### ブログ記事
- **配置場所**: `src/content/posts/`
- **ファイル形式**: Markdown (`.md`)
- **命名規則**: `YYYY-MM-DD_記事名.md`
- **新規作成**: 必ず`pnpm new`コマンドを使用（手動作成禁止）

### フロントマター必須項目
```yaml
---
title: 記事タイトル
pubDate: YYYY-MM-DD
description: 記事の概要
tags: ["タグ1", "タグ2"]
---
```

**注意**: Claude Codeで生成・編集した記事には `Claude_Code` タグを追加すること。

## ディレクトリ構成

```
hirom.net/
├── src/
│   ├── components/
│   │   ├── ui/           # 再利用可能UIコンポーネント
│   │   └── layout/       # レイアウトコンポーネント
│   ├── content/
│   │   └── posts/        # ブログ記事
│   ├── pages/            # ページコンポーネント
│   └── styles/
│       └── global.css    # グローバルスタイル
├── public/               # 静的ファイル
└── scripts/              # ユーティリティスクリプト
```

## コードスタイル

- **フォーマット**: Prettierで整形（コミット前に`pnpm format`）
- **リント**: ESLintチェック必須（`pnpm lint`）
- **コンポーネントスタイル**: Astroコンポーネント内の`<style>`タグでスコープ化

## 依存関係管理

```bash
pnpm add パッケージ名        # 本番依存追加
pnpm add -D パッケージ名     # 開発依存追加
```

## デプロイ

- **ホスティング**: Netlify
- **自動デプロイ**: `main`ブランチへのpushで自動実行
- **ビルドコマンド**: `pnpm build`

---
*最終更新: 2025-12-07*
