# 濱口デザインサービス - WEBサイトパッケージ

## 📦 パッケージ内容

このパッケージには、濱口デザインサービスのプロフェッショナルなポートフォリオサイトが含まれています。

### ファイル一覧

1. **standalone.html** ⭐ 推奨
   - 完全なスタンドアロンHTMLファイル
   - 外部依存関係なし
   - Cloudflare Pages へのデプロイが最も簡単
   - ファイルサイズ: 約50KB（軽量）

2. **DEPLOYMENT_GUIDE.md**
   - Cloudflare Pages へのデプロイ手順
   - カスタマイズ方法
   - トラブルシューティング

3. **README.md** （このファイル）
   - パッケージ概要

## 🚀 クイックスタート

### 最速デプロイ方法（1分以内）

1. **Cloudflare にアクセス**
   - https://dash.cloudflare.com/ にログイン

2. **Pages プロジェクトを作成**
   - 左メニュー → Pages → プロジェクトを作成

3. **ファイルをアップロード**
   - 「アップロード」タブを選択
   - `standalone.html` をドラッグ&ドロップ
   - プロジェクト名を入力
   - 「デプロイ」をクリック

4. **完了！**
   - 自動生成されたURLでサイトが公開されます

## ✨ 主な機能

- ✅ **レスポンシブデザイン** - スマートフォン・タブレット・デスクトップ対応
- ✅ **スムーズなスクロール** - モダンなアニメーション
- ✅ **高速ロード** - 最適化されたコード
- ✅ **SEO対応** - 検索エンジン最適化済み
- ✅ **モバイルメニュー** - タッチフレンドリーなナビゲーション
- ✅ **ダークモード対応** - 目に優しい表示

## 🎨 デザイン特性

- **色合い**: 石色（Stone）を基調とした落ち着いた配色
- **フォント**: Noto Serif JP / Noto Sans JP（日本語最適化）
- **レイアウト**: モダンで洗練されたグリッドシステム
- **インタラクション**: スムーズなホバーエフェクトと遷移

## 📝 カスタマイズ例

### テキスト変更
`standalone.html` をテキストエディタで開き、以下を編集：
- 「濱口デザインサービス」→ 自社名
- 「info@hamaguchi-design.jp」→ 自社メールアドレス
- 「〒213-0022 神奈川県...」→ 自社住所

### 色変更
CSS の `:root` セクションの色コードを変更：
```css
--stone-900: #1c1917;  /* 黒色 */
--stone-50: #fafaf8;   /* 白色 */
```

### ソーシャルリンク更新
```html
<a href="https://www.instagram.com/your-account">
```

## 📱 対応ブラウザ

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## 🔧 トラブルシューティング

**Q: デプロイ後、サイトが表示されない**
- A: ブラウザキャッシュをクリア（Ctrl+Shift+Delete）

**Q: 画像が表示されない**
- A: 画像URLを確認し、正しいパスに変更

**Q: カスタムドメインを設定したい**
- A: DEPLOYMENT_GUIDE.md の「カスタムドメイン設定」セクションを参照

## 💡 ベストプラクティス

1. **定期的なバックアップ**
   - `standalone.html` をローカルに保存

2. **パフォーマンス最適化**
   - 画像は WebP 形式を使用
   - 不要なスクリプトは削除

3. **SEO最適化**
   - メタディスクリプション を追加
   - Open Graph タグを設定

## 📚 参考リソース

- [Cloudflare Pages 公式ドキュメント](https://developers.cloudflare.com/pages/)
- [HTML/CSS リファレンス](https://developer.mozilla.org/ja/)
- [Web デザインベストプラクティス](https://web.dev/)

## 📄 ライセンス

このプロジェクトは MIT ライセンスの下で公開されています。

## 🤝 サポート

ご質問や問題がある場合：
1. DEPLOYMENT_GUIDE.md を確認
2. Cloudflare サポート: https://support.cloudflare.com/
3. コミュニティフォーラム: https://community.cloudflare.com/

## 📞 連絡先

- メール: info@hamaguchi-design.jp
- Instagram: @hamaguchi_design

---

**バージョン**: 1.0.0  
**最終更新**: 2024年3月  
**作成**: Hamaguchi Design Service
