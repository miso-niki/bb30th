# bb30th

株式会社ビジネスバンク 創業30周年記念 大同窓会（2027年2月7日・青山）の案内ページ。

- 公開URL（試験）: https://miso-niki.github.io/bb30th/
- 公開URL（本番予定）: https://bb30th.jp/

## 構成

| ファイル | 中身 |
|---|---|
| `index.html` | 写真・ロゴを埋め込んだ単体ページ |
| `ogp.png` | LINE / X 共有時のサムネイル（1200x630） |
| `.nojekyll` | GitHub Pages の前処理を無効化 |

## 更新のしかた

このリポジトリは書き出し先です。編集は Claude Design 側で行い、
`~/Documents/Claude/Projects/bb30-lp/` でビルドし直して push します。

```
python3 build.py --base https://bb30th.jp --out deploy/index.html
```

試験公開のあいだは `--noindex` を付けて検索避けを入れています。
本番公開時は外してください。
