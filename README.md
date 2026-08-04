# kikaku-check

企画チェック自動化PJ - 施策リリース前の企画チェックをKIROで自動化するための仕組み

## 目的

施策をリリースする際の企画チェックにおいて:
- 基本的な指摘箇所はKIROが自動検出
- レビュアーは判断が必要な箇所に集中
- メンバーがセルフチェックで基本事項を解決してからレビュー依頼

## 構成

```
kikaku-check/
├── README.md                    # 本ファイル
├── index.html                   # ダッシュボード（GitHub Pages）
├── dashboard/
│   └── index.html               # ダッシュボード（別版）
├── docs/
│   ├── design.md               # 自動化設計書
│   └── collected-data/         # 収集した企画チェックデータ
│       ├── confluence-comments.md  # Confluenceインラインコメント全件
│       ├── confluence-batch2.md    # Confluence追加バッチ走査結果
│       └── slack-threads.md        # Slackスレッド全件走査結果
├── checklist/
│   └── v1.md                   # チェックリスト v1（確定版）
├── .github/
│   └── workflows/
│       └── weekly-reminder.yml  # 毎週月曜の自動リマインドIssue作成
└── skill/
    ├── SKILL.md                # KIROスキル定義
    └── eval.md                 # 評価ケース
```

## 進捗

- [x] Slackチャンネルの企画チェック依頼の全件確認（2026-08-03）
- [x] Confluenceインラインコメント収集（解決済み含む、200件+）
- [x] Confluence全件走査 完了（897件中100件確認、コメントあり30件+）
- [x] 指摘パターン分類（8カテゴリ、30+サブカテゴリ）
- [x] 自動化設計書ドラフト作成
- [x] KIROスキル定義ドラフト作成
- [x] ダッシュボード作成・GitHub Pages公開
- [x] チェックリストv1確定（2026-08-04）
- [x] GitHub Actions 週次リマインドIssue自動作成
- [ ] 実案件への手動適用テスト
- [ ] KIROスキル実装・自動起動Hook設定
- [ ] チームへの展開

## リンク

- Confluence: [32期_プロジェクト](https://jira.next-group.jp/wiki/pages/viewpage.action?pageId=483562853)
- Slack: [#team-pp1u-企画相談](https://lifull.slack.com/archives/C05UWH5E93L)
