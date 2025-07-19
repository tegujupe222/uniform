# 制服ARカメラ

リアルタイムで制服のARオーバーレイを表示できるWebアプリケーションです。

## 機能

- 📱 リアルタイムカメラフィード
- 👔 男子・女子制服の切り替え
- 🎯 ドラッグ&ドロップで位置調整
- 📏 スケール調整スライダー
- 📸 写真撮影・保存機能
- 📱 モバイル対応

## 技術スタック

- HTML5
- CSS3
- JavaScript (ES6+)
- WebRTC (getUserMedia API)
- Canvas API

## セットアップ

### ローカル開発

1. リポジトリをクローン
```bash
git clone https://github.com/yourusername/uniform-ar-camera.git
cd uniform-ar-camera
```

2. ローカルサーバーを起動
```bash
# Node.jsの場合（推奨）
npm install
npm run dev

# Python 3の場合
python -m http.server 8000

# その他の方法
npx serve .
```

3. `http://localhost:3000` にアクセス

### Vercelデプロイ

このプロジェクトはVercelでデプロイされています。

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/yourusername/uniform-ar-camera)

#### 手動デプロイ手順

1. [Vercel](https://vercel.com) にアカウントを作成
2. GitHubリポジトリをインポート
3. プロジェクト設定で以下を確認：
   - Framework Preset: Other
   - Build Command: `npm run build`
   - Output Directory: `.`
4. デプロイボタンをクリック

## 使用方法

1. カメラの使用許可を許可してください
2. 制服の種類を選択（男子/女子）
3. ドラッグして制服の位置を調整
4. スライダーでサイズを調整
5. 撮影ボタンで写真を保存

## ブラウザ対応

- Chrome 53+
- Firefox 36+
- Safari 11+
- Edge 79+

## ライセンス

MIT License

## 貢献

プルリクエストやイシューの報告を歓迎します！ 