# README

mkdocsを使ったドキュメンテーションビルドの環境をCircleCIに乗せて色々自動化する。

## 注釈
2/26現在、CircleCIコンフィグは試行錯誤の検証中です。

ブランチはmaster/developの2つあり、それぞれにpushすると次のような動作をするよう設定しています。

### master
`mkdocs build` が成功したらS3へデプロイ

### develop
`mkdocs build` の成功後に「承認プロセス」を挟む。

実際の承認フローの前に、Slack webhookを使って承認確認画面へのリンクを通知するようなワークフローを組んでいる。