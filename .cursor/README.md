# Cursor Rules Documentation

このディレクトリには、プロジェクト開発における行動指針とベストプラクティスを定義したCursor Rulesが含まれています。

## 📁 ディレクトリ構造

```
.cursor/
├── README.md                           # このファイル - ルール全体の説明
├── REFACTORING_SUMMARY.md             # 最新のリファクタリング内容の詳細
└── rules/
    ├── django-development.mdc         # Django開発の包括的ガイドライン
    └── playwright-visual-development.mdc  # Playwright MCPによる視覚的開発・テスト指針
```

## 🎯 ルール概要

### Django Development Rules
**ファイル**: `rules/django-development.mdc`
**適用**: 常時適用 (`alwaysApply: true`)

Django開発のための包括的なガイドラインを提供します：

- **フレームワーク選択基準**: 最新安定版Django、DRF使用
- **プロジェクト構造**: 推奨ディレクトリ構成とファイル配置
- **開発標準**: コーディング規約、命名規則、型ヒント
- **セキュリティ**: CSRF保護、認証・認可、入力検証
- **外部アクセス設定**: ngrok/トンネリング設定の詳細手順
- **データベース設定**: 環境別データベース構成
- **API開発**: DRFを使用したRESTful API設計
- **エラーハンドリング**: ログ設定と例外処理
- **テスト戦略**: 単体・統合・E2Eテストの実装方針
- **パフォーマンス最適化**: キャッシュ、クエリ最適化
- **デプロイメント**: 本番環境への配置考慮事項

### Playwright Visual Development Rules
**ファイル**: `rules/playwright-visual-development.mdc`
**適用**: 常時適用 (`alwaysApply: true`)

Playwright MCPを使用した視覚的開発・テストの指針：

- **核心原則**: 視覚的確認を重視した開発フロー
- **開発ワークフロー**: 実装→サーバー起動→視覚確認→反復改善
- **MCP ツール使用法**: 
  - ナビゲーション・ページ管理
  - 視覚的検証・スクリーンショット
  - ユーザーインタラクション
  - 高度な操作
  - デバッグ・モニタリング
- **テスト戦略**: 体系的なテスト計画とワークフロー
- **ドキュメント管理**: スクリーンショット管理と課題追跡
- **Django統合テスト**: 管理画面、API、認証フローの具体的テストシナリオ

## 🚀 ルールの使用方法

### 自動適用
すべてのルールは `alwaysApply: true` が設定されており、Cursorが自動的に適用します。

### 手動参照
開発中に特定のガイドラインを確認したい場合：

1. **Django開発**: `.cursor/rules/django-development.mdc` を参照
2. **視覚的テスト**: `.cursor/rules/playwright-visual-development.mdc` を参照
3. **リファクタリング履歴**: `.cursor/REFACTORING_SUMMARY.md` を参照

### 実践的な使用例

#### Django新機能開発時
```markdown
1. django-development.mdc の「開発標準」を確認
2. プロジェクト構造に従ってファイル配置
3. セキュリティガイドラインに従って実装
4. playwright-visual-development.mdc に従って視覚的確認
```

#### ngrokを使用した外部公開時
```markdown
1. django-development.mdc の「外部アクセス設定」セクション参照
2. settings.py に指定の設定を追加
3. Django開発サーバーを再起動
4. ngrok起動後、視覚的テストで動作確認
```

#### API開発時
```markdown
1. django-development.mdc の「API開発」セクション確認
2. DRFのベストプラクティスに従って実装
3. playwright-visual-development.mdc でフロントエンド連携テスト
4. ネットワークモニタリングでAPI動作確認
```

## 🔄 ルールの更新・メンテナンス

### 定期見直し
- **四半期ごと**: Django・ツールバージョンとの整合性確認
- **プロジェクト固有追加**: 必要に応じて現在の構造を維持しながら追加
- **ツール更新**: MCP Playwrightツール更新時の対応
- **ベストプラクティス進化**: チーム学習と業界標準の継続的更新

### 変更履歴の追跡
重要な変更は `REFACTORING_SUMMARY.md` に記録し、変更理由と影響を文書化しています。

## ❓ よくある質問

### Q: ルールが適用されない場合は？
A: Cursorの設定でルール適用が有効になっているか確認してください。また、ファイルの`alwaysApply: true`設定を確認してください。

### Q: プロジェクト固有のルールを追加したい場合は？
A: 現在の2ファイル構造を維持し、該当セクションに追加することをお勧めします。大幅な追加の場合は新ファイル作成も検討してください。

### Q: ルールの内容が古くなった場合は？
A: `REFACTORING_SUMMARY.md`を参考に、適切なセクションを更新し、変更履歴を記録してください。

## 📚 関連リソース

- [Django公式ドキュメント](https://docs.djangoproject.com/)
- [Django REST Framework](https://www.django-rest-framework.org/)
- [Playwright公式ドキュメント](https://playwright.dev/)
- [ngrok公式ドキュメント](https://ngrok.com/docs)

---

**最終更新**: 2025年1月
**メンテナンス責任**: 開発チーム
