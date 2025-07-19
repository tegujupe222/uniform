# Vercelデプロイメントガイド

## 前提条件

- GitHubアカウント
- Vercelアカウント（無料で作成可能）

## デプロイ手順

### 1. GitHubリポジトリの作成

1. [GitHub](https://github.com) にログイン
2. 新しいリポジトリを作成（例：`uniform-ar-camera`）
3. 以下のコマンドでリモートリポジトリを追加：

```bash
git remote add origin https://github.com/YOUR_USERNAME/uniform-ar-camera.git
git branch -M main
git push -u origin main
```

### 2. Vercelでのデプロイ

#### 方法1: Vercel CLIを使用（推奨）

1. Vercel CLIをインストール：
```bash
npm i -g vercel
```

2. プロジェクトディレクトリでログイン：
```bash
vercel login
```

3. デプロイ：
```bash
vercel
```

4. 本番環境にデプロイ：
```bash
vercel --prod
```

#### 方法2: Vercel Web UIを使用

1. [Vercel](https://vercel.com) にアクセス
2. "New Project" をクリック
3. GitHubリポジトリをインポート
4. プロジェクト設定：
   - **Framework Preset**: Other
   - **Build Command**: `npm run build`
   - **Output Directory**: `.`
   - **Install Command**: `npm install`
5. "Deploy" をクリック

### 3. カスタムドメインの設定（オプション）

1. Vercelダッシュボードでプロジェクトを選択
2. "Settings" → "Domains"
3. カスタムドメインを追加

## 環境変数

このプロジェクトは現在環境変数を必要としませんが、将来的に追加する場合は：

1. Vercelダッシュボード → "Settings" → "Environment Variables"
2. 必要な環境変数を追加

## トラブルシューティング

### よくある問題

1. **HTTPSエラー**: Vercelは自動的にHTTPSを提供
2. **カメラ権限**: ブラウザでカメラ権限を許可する必要があります
3. **画像読み込みエラー**: `boy.png`と`girl.png`が正しく配置されていることを確認

### デバッグ方法

1. ブラウザの開発者ツールでコンソールエラーを確認
2. Vercelのデプロイログを確認
3. ローカルでテストしてからデプロイ

## 更新と再デプロイ

コードを更新した場合：

```bash
git add .
git commit -m "Update description"
git push origin main
```

Vercelは自動的に新しいデプロイを開始します。

## パフォーマンス最適化

- 画像ファイルの最適化
- ブラウザキャッシュの活用
- CDNの活用（Vercelが自動で提供）

## セキュリティ

- HTTPSが自動で有効
- セキュリティヘッダーが設定済み
- カメラアクセスはユーザー許可が必要 