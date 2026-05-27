# skill-kindle-capture

Claude Code 用の Kindle PDF 化補助 Skill。Kindle Web Reader（read.amazon.co.jp）と Kindle macOS アプリの両方から、書籍のスクリーンショットを連続キャプチャして PDF 化するためのガイドと運用ルールを Claude に教える。

## 注意：これは私的バックアップ用の運用メモです

- 個人で購入した Kindle 本を**自分用にバックアップ**することを想定したスキルです
- **再配布・販売・社外共有は禁止**です（著作権法上、私的使用の範囲を超える行為になります）
- このリポジトリで配布しているのは **Claude Code への指示書だけ** で、実際のキャプチャ処理を行う外部ツール（[`Tsunoda-s-FT/kindle-app`](https://github.com/Tsunoda-s-FT/kindle-app)）は別途ローカルに clone する必要があります

## インストール

```bash
git clone https://github.com/sasaki-ta-instyle/skill-kindle-capture \
  ~/.claude/skills/kindle-capture
```

Claude Code を再起動すれば、自然言語で次のように頼めるようになる。

```
Kindle で読んでる「○○」を PDF にして
```

その後、Claude が `Tsunoda-s-FT/kindle-app` のセットアップ手順から PDF 出力までを順に案内してくれる。

## 同梱ドキュメント

| ファイル | 内容 |
|---|---|
| [`SKILL.md`](./SKILL.md) | エージェント運用ルール・モード判定・呼び出しコマンド |
| [`REFERENCE.md`](./REFERENCE.md) | コマンドラインオプションのリファレンス |
| [`EXAMPLES.md`](./EXAMPLES.md) | よく使う組み合わせの実例集 |

## ライセンス

MIT License — [`LICENSE`](./LICENSE) を参照。

ライセンス対象は **本リポジトリに含まれる Markdown 文書のみ**。実際の Kindle キャプチャ処理を担う `Tsunoda-s-FT/kindle-app` は別リポジトリ・別ライセンスです。
