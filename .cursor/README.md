# Cursor Rules Documentation

このディレクトリには、プロジェクト開発における行動指針とベストプラクティスを定義したCursor Rulesが含まれています。

## 📁 ディレクトリ構造

```
.cursor/
├── README.md                           # このファイル - ルール全体の説明
├── REFACTORING_SUMMARY.md             # 最新のリファクタリング内容の詳細
├── mcp.json                           # MCP サーバー設定
└── rules/
    ├── django-development.mdc         # Django開発の包括的ガイドライン (Context7 MCP統合)
    ├── playwright-visual-development.mdc  # Playwright MCPによる視覚的開発・テスト指針
    ├── context7-mcp-usage.mdc         # Context7 MCP専用使用ガイドライン
    └── mcp-integration.mdc            # MCP統合戦略とワークフロー
```

## 🎯 ルール概要

### Django Development Rules
**ファイル**: `rules/django-development.mdc`
**適用**: 常時適用 (`alwaysApply: true`)

Django開発のための包括的なガイドラインを提供します：

- **Context7 MCP統合**: 全開発フローでContext7 MCPを主要ドキュメント源として活用
- **フレームワーク選択基準**: 最新安定版Django、DRF使用
- **プロジェクト構造**: 推奨ディレクトリ構成とファイル配置
- **開発標準**: コーディング規約、命名規則、型ヒント
- **ドキュメント戦略**: Context7 MCPによるリアルタイム情報アクセス
- **セキュリティ**: CSRF保護、認証・認可、入力検証
- **外部アクセス設定**: ngrok/トンネリング設定の詳細手順
- **データベース設定**: 環境別データベース構成
- **API開発**: Context7 MCP参照によるDRFパターン実装
- **エラーハンドリング**: ログ設定と例外処理
- **テスト戦略**: 単体・統合・E2Eテストの実装方針
- **パフォーマンス最適化**: Context7 MCP活用によるDjango最適化パターン
- **デプロイメント**: 本番環境への配置考慮事項

### Playwright Visual Development Rules
**ファイル**: `rules/playwright-visual-development.mdc`
**適用**: 常時適用 (`alwaysApply: true`)

Playwright MCPを使用した視覚的開発・テストの指針：

- **核心原則**: Context7 MCP連携による視覚的確認重視の開発フロー
- **開発ワークフロー**: Context7リサーチ→実装→サーバー起動→視覚確認→反復改善
- **MCP ツール使用法**: 
  - ナビゲーション・ページ管理
  - 視覚的検証・スクリーンショット
  - ユーザーインタラクション
  - 高度な操作
  - デバッグ・モニタリング
- **テスト戦略**: Context7 MCP研究を組み込んだ体系的テスト計画
- **ドキュメント管理**: スクリーンショット管理と課題追跡
- **Django統合テスト**: 管理画面、API、認証フローの具体的テストシナリオ

### Context7 MCP Usage Rules
**ファイル**: `rules/context7-mcp-usage.mdc`
**適用**: 常時適用 (`alwaysApply: true`)

Context7 MCPの効率的な使用方法を定義：

- **主要戦略**: Context7 MCPを全ライブラリドキュメントの第一選択肢として活用
- **ライブラリ解決ワークフロー**: ライブラリ特定から文書取得までの段階的プロセス
- **文書取得ベストプラクティス**: トークン最適化と対象絞り込み検索
- **統合ポイント**: Django、Playwright、パフォーマンス最適化の具体的ガイダンス
- **品質保証**: 検証戦略とクロスリファレンス手法

### MCP Integration Rules
**ファイル**: `rules/mcp-integration.mdc`
**適用**: 常時適用 (`alwaysApply: true`)

複数MCPサーバーの統合戦略：

- **MCPエコシステム**: Context7、Playwright、DeepWiki MCPの協調使用
- **開発ワークフローフェーズ**: リサーチ→実装→視覚確認→ドキュメント化
- **クロスMCPワークフロー**: Django API開発とパフォーマンス最適化の具体的パターン
- **品質保証**: 複数MCPサーバーを活用した包括的テスト戦略
- **トラブルシューティング**: MCPサーバー問題とフォールバック戦略

## 🚀 ルールの使用方法

### 自動適用
すべてのルールは `alwaysApply: true` が設定されており、Cursorが自動的に適用します。

### 手動参照
開発中に特定のガイドラインを確認したい場合：

1. **Django開発**: `.cursor/rules/django-development.mdc` を参照
2. **視覚的テスト**: `.cursor/rules/playwright-visual-development.mdc` を参照
3. **Context7 MCP使用**: `.cursor/rules/context7-mcp-usage.mdc` を参照
4. **MCP統合戦略**: `.cursor/rules/mcp-integration.mcp` を参照
5. **リファクタリング履歴**: `.cursor/REFACTORING_SUMMARY.md` を参照

### 実践的な使用例

#### Django新機能開発時
```markdown
1. context7-mcp-usage.mdc でContext7 MCPワークフローを確認
2. Context7 MCPでDjango関連ライブラリとパターンをリサーチ
3. django-development.mdc の「開発標準」を確認
4. プロジェクト構造に従ってファイル配置
5. セキュリティガイドラインに従って実装
6. playwright-visual-development.mdc に従って視覚的確認
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
1. Context7 MCPでDRFパターンとベストプラクティスをリサーチ
2. django-development.mdc の「API開発」セクション確認
3. Context7ガイドに従ってDRFを実装
4. playwright-visual-development.mcp でフロントエンド連携テスト
5. ネットワークモニタリングでAPI動作確認
6. Context7 MCPでテストパターンを参照して包括的テスト実装
```

## 🔄 ルールの更新・メンテナンス

### 定期見直し
- **四半期ごと**: Django・ツールバージョンとの整合性確認
- **Context7 MCP最新化**: Context7 MCPの新機能とライブラリ更新の反映
- **プロジェクト固有追加**: 必要に応じて現在の構造を維持しながら追加
- **ツール更新**: MCP Playwrightツール更新時の対応
- **ベストプラクティス進化**: Context7 MCPから得られる最新パターンの継続的更新

### 変更履歴の追跡
重要な変更は `REFACTORING_SUMMARY.md` に記録し、変更理由と影響を文書化しています。

## ❓ よくある質問

### Q: ルールが適用されない場合は？
A: Cursorの設定でルール適用が有効になっているか確認してください。また、ファイルの`alwaysApply: true`設定を確認してください。

### Q: プロジェクト固有のルールを追加したい場合は？
A: 現在の4ファイル構造を維持し、該当セクションに追加することをお勧めします。Context7 MCP関連の追加は適切なファイルに追加してください。大幅な追加の場合は新ファイル作成も検討してください。

### Q: ルールの内容が古くなった場合は？
A: `REFACTORING_SUMMARY.md`を参考に、適切なセクションを更新し、変更履歴を記録してください。

## 📚 関連リソース

### 主要リソース（Context7 MCP経由アクセス推奨）
- **Django**: Context7 MCPで `django` を検索
- **Django REST Framework**: Context7 MCPで `django-rest-framework` を検索  
- **Playwright**: Context7 MCPで `playwright` を検索

### 補完リソース
- [Django公式ドキュメント](https://docs.djangoproject.com/)
- [Django REST Framework](https://www.django-rest-framework.org/)
- [Playwright公式ドキュメント](https://playwright.dev/)
- [ngrok公式ドキュメント](https://ngrok.com/docs)

### MCP設定
- `mcp.json`: Context7、Playwright、DeepWiki MCP サーバー設定

---

**最終更新**: 2025年1月 - Context7 MCP統合
**メンテナンス責任**: 開発チーム
