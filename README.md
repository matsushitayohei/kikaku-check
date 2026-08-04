# kikaku-check

企画チェック自動化PJ - 施策リリース前の企画チェックをKIROで自動化するための仕組み

## 目的

施策をリリースする際の企画チェックにおいて:
- 基本的な指摘箇所はKIROが自動検出
- レビュアーは判断が必要な箇所に集中
- メンバーがセルフチェックで基本事項を解決してからレビュー依頼

## 構成

`
kikaku-check/
├── README.md                    # 本ファイル
├── docs/
│   ├── design.md               # 自動化設計書
│   └── collected-data/         # 収集した企画チェックデータ
│       ├── confluence-comments.md  # Confluenceインラインコメント全件
│       └── slack-threads.md        # Slackスレッドの議論
├── checklist/
│   ├── common.md               # 全施策共通チェックリスト
│   ├── cro.md                  # CRO施策向け
│   ├── seo.md                  # SEO施策向け
│   ├── revenue.md              # 売上施策向け
│   └── b2b.md                  # B2B施策向け
└── skill/
    ├── SKILL.md                # KIROスキル定義
    └── eval.md                 # 評価ケース
`

## 進捗

- [x] Slackチャンネルの企画チェック依頼の全件確認（2026-08-03）
- [x] Confluenceインラインコメント収集（解決済み含む、115件+）
- [x] 指摘パターン分類（8カテゴリ、30+サブカテゴリ）
- [x] 自動化設計書ドラフト作成
- [x] KIROスキル定義ドラフト作成
- [ ] Confluence全ページ（897件）のコメント全件走査
- [ ] チェックリストv1確定
- [ ] 実案件への手動適用テスト
- [ ] KIROスキル実装・自動起動Hook設定
- [ ] チームへの展開

## リンク

- Confluence: [32期_プロジェクト](https://jira.next-group.jp/wiki/pages/viewpage.action?pageId=483562853)
- Slack: [#team-pp1u-企画相談](https://lifull.slack.com/archives/C05UWH5E93L)
