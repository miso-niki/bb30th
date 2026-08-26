# bb30th

株式会社ビジネスバンク 創業30周年記念 大同窓会（2027年2月7日・青山）の案内ページ。

- **公開URL: https://bb30th.jp/**
- `www.bb30th.jp` と旧 `miso-niki.github.io/bb30th` は自動で上へ転送される

## 構成

| ファイル | 中身 |
|---|---|
| `index.html` | 写真・ロゴを埋め込んだ単体ページ |
| `ogp-v3.png` | LINE / X 共有時のサムネイル（1200x630）。作り直したらファイル名を変える（SNSはURL単位でキャッシュするため） |
| `ogp.png` / `ogp-v2.png` | 旧サムネイル。すでに共有されたリンクのために残してある |
| `CNAME` | 独自ドメインの指定（GitHub Pages が読む） |
| `.nojekyll` | GitHub Pages の前処理を無効化 |

## 更新のしかた

このリポジトリは書き出し先。編集は Claude Design 側で行い、
`~/Documents/Claude/Projects/bb30-lp/` でビルドし直して push する。

```
python3 build.py --base https://bb30th.jp --noindex --out deploy/index.html
```

**試験公開のあいだは `--noindex` を付けている。正式案内を出すときに外す。**
外すと「ビジネスバンク 30周年」で検索したOBがたどり着けるようになる。

OB・OG企業の一覧はスプレッドシートから実行時に読むので、
掲載が増えてもビルドし直す必要はない（手順は親フォルダの README）。
