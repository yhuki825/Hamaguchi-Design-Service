# 濱口デザインサービス - Cloudflare Pages デプロイガイド

## 概要

このパッケージには、濱口デザインサービスのポートフォリオサイトの2つのバージョンが含まれています：

1. **standalone.html** - スタンドアロン版（推奨）
   - 単一のHTMLファイル
   - 外部依存関係なし
   - 最速のデプロイ

2. **React版** - フル機能版
   - React + Tailwind CSS
   - より高度なカスタマイズが可能
   - ビルドプロセスが必要

## Cloudflare Pages へのデプロイ方法

### 方法1: スタンドアロン版（最も簡単）

#### ステップ1: Cloudflare アカウントにログイン
- [Cloudflare Dashboard](https://dash.cloudflare.com/) にアクセス
- アカウントにログイン

#### ステップ2: Pages プロジェクトを作成
1. 左側メニューから「Pages」を選択
2. 「プロジェクトを作成」をクリック
3. 「アップロード」タブを選択

#### ステップ3: ファイルをアップロード
1. `standalone.html` ファイルをアップロード
2. プロジェクト名を入力（例：`hamaguchi-design`）
3. 「デプロイ」をクリック

#### ステップ4: カスタムドメイン設定（オプション）
1. デプロイ後、プロジェクト設定を開く
2. 「カスタムドメイン」セクションで独自ドメインを設定

### 方法2: React版（Git統合）

#### ステップ1: リポジトリを準備
```bash
# プロジェクトディレクトリに移動
cd hamaguchi-design-service

# Git初期化
git init
git add .
git commit -m "Initial commit"
```

#### ステップ2: GitHub にプッシュ
1. GitHub で新しいリポジトリを作成
2. ローカルリポジトリをプッシュ

```bash
git remote add origin https://github.com/your-username/hamaguchi-design.git
git branch -M main
git push -u origin main
```

#### ステップ3: Cloudflare Pages で接続
1. Cloudflare Dashboard > Pages
2. 「プロジェクトを作成」> 「Git に接続」
3. GitHub アカウントを認証
4. リポジトリを選択

#### ステップ4: ビルド設定
- **フレームワークプリセット**: React
- **ビルドコマンド**: `npm run build`
- **ビルド出力ディレクトリ**: `dist/public`

#### ステップ5: デプロイ
「保存してデプロイ」をクリック

## ファイル構成

```
hamaguchi-design-service/
├── standalone.html          ← Cloudflare Pages用（推奨）
├── client/
│   ├── src/
│   │   ├── pages/
│   │   │   └── Home.tsx     ← メインコンポーネント
│   │   ├── index.css        ← グローバルスタイル
│   │   └── main.tsx
│   ├── index.html
│   └── public/
├── package.json
├── DEPLOYMENT_GUIDE.md      ← このファイル
└── README.md
```

## カスタマイズ方法

### スタンドアロン版の編集
`standalone.html` をテキストエディタで直接編集：

1. **テキスト内容の変更**
   - HTML内の日本語テキストを編集
   - 例：「濱口デザインサービス」を別の名前に変更

2. **色の変更**
   - `:root` セクションの `--stone-*` 変数を編集
   - または、各要素の `background-color` を直接変更

3. **フォントの変更**
   - `<link>` タグで Google Fonts を変更
   - CSS の `font-family` を更新

4. **ソーシャルリンク更新**
   - `href="https://www.instagram.com/"` を実際のURLに変更
   - メールアドレスを `info@hamaguchi-design.jp` から変更

### React版の編集
1. `client/src/pages/Home.tsx` を編集
2. `npm run dev` でローカルプレビュー
3. `npm run build` でビルド
4. Git でプッシュ（自動デプロイ）

## トラブルシューティング

### デプロイが失敗する場合
1. ファイルサイズを確認（100MB以下）
2. ファイル名に特殊文字がないか確認
3. HTMLの構文エラーをチェック

### サイトが表示されない場合
1. ブラウザキャッシュをクリア
2. Cloudflare の DNS キャッシュをクリア
3. ドメイン設定を確認

### パフォーマンスが遅い場合
- 画像を最適化（WebP形式推奨）
- 不要なスクリプトを削除
- CDN キャッシュを有効化

## サポート

### Cloudflare Pages ドキュメント
- [Cloudflare Pages 公式ドキュメント](https://developers.cloudflare.com/pages/)
- [デプロイメント ガイド](https://developers.cloudflare.com/pages/platform/deploy-builds/)

### 技術サポート
- Cloudflare サポート: https://support.cloudflare.com/
- コミュニティフォーラム: https://community.cloudflare.com/

## ライセンス

このプロジェクトは MIT ライセンスの下で公開されています。

## 変更履歴

### v1.0.0 (2024年)
- 初回リリース
- スタンドアロン版作成
- React版完成
- Cloudflare Pages 対応

---

**最終更新**: 2024年
**作成者**: Hamaguchi Design Service
