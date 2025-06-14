# 新規記事作成ワークフロー

## トリガー
ユーザーが「新規記事作成」と入力した時

## 実行手順

### 1. 歓迎メッセージ
```
新しい記事の作成を開始しますね！
まずは、記事のテーマやアイデアについて教えてください。
```

### 2. 情報収集対話
以下の情報を対話形式で収集：

#### 基本情報
- **記事テーマ**: 何について書きたいか
- **記事タイプ**: ノウハウ、体験談、考察、レビューなど
- **想定読者**: ターゲット層
- **記事の目的**: 何を伝えたいか、読者にどうなってほしいか

#### 詳細情報
- **具体的なポイント**: 特に強調したい内容
- **個人的体験**: 実体験やエピソード
- **参考にしたい記事**: 過去の自分の記事で参考にしたいもの
- **締切や公開予定**: いつ頃投稿したいか

### 3. 情報整理・確認
収集した情報をまとめて確認：
```
記事の企画内容を整理させていただきました：

【記事テーマ】: [テーマ]
【記事タイプ】: [タイプ]
【想定読者】: [読者層]
【記事の目的】: [目的]
【具体的なポイント】: [ポイント]
【個人的体験】: [体験]
【参考記事】: [参考]
【公開予定】: [締切]

この内容で進めてよろしいでしょうか？
修正がある場合はお知らせください。
```

### 4. プロジェクトファイル作成
`articles/drafts/` フォルダに以下のファイルを作成：
```
YYYY-MM-DD_[記事タイトル]/
├── article_info.md    # 企画情報
├── research_notes.md  # 調査メモ  
├── outline.md         # 記事構成
└── draft.md          # 記事本文
```

### 5. 次ステップ案内
```
記事企画の準備が完了しました！
次は「情報収集」で過去記事の分析と最新情報の収集を行いましょう。

または、すぐに執筆を始めたい場合は「記事執筆」をお試しください。
```

## 生成ファイル

### article_info.md テンプレート
```markdown
# 記事企画情報

## 基本情報
- **作成日**: [日付]
- **記事テーマ**: [テーマ]
- **記事タイプ**: [タイプ]
- **想定読者**: [読者層]
- **記事の目的**: [目的]

## 内容詳細
- **具体的なポイント**: [ポイント]
- **個人的体験**: [体験]
- **参考記事**: [参考]
- **公開予定**: [締切]

## ステータス
- **現在のフェーズ**: 企画完了
- **進捗**: 企画情報収集完了
- **次のアクション**: 情報収集または記事執筆

## メモ
- [その他のメモや気づき]
```

## エラーハンドリング
- 必要な情報が不足している場合は、追加の質問を行う
- ユーザーが中断したい場合は、進捗を保存して終了する
- 既存の記事と重複する場合は、確認を取る 