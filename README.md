# zenn-content

[Zenn](https://zenn.dev) の記事を管理するリポジトリ。GitHub 連携でこのリポジトリの `main` に push すると Zenn に自動同期される。

## 構成

- `articles/` … 記事（Markdown）。1ファイル = 1記事。
- `books/` … 本（複数チャプター）。

## よく使うコマンド

```bash
# 新しい記事を作成
npx zenn new:article

# ローカルプレビュー（http://localhost:8000）
npx zenn preview

# 記事一覧
npx zenn list:articles
```

## 公開フロー

1. `articles/` の Markdown を編集する。
2. フロントマターの `published` を `true` にする（公開したいとき）。`false` の間は同期されても下書き扱いで非公開。
3. `main` に push すると Zenn が自動で同期する（GitHub 連携が設定済みの場合）。

## GitHub 連携の設定

Zenn ダッシュボード → アカウント → 「GitHubからのデプロイ」からこのリポジトリを連携する。詳細は記事公開時に。
