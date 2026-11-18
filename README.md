# checkers-rom (monorepo)

Amazon Echo Show 5 (1st gen / codename **`checkers`**) 向けの
**軽量スマートディスプレイ ROM** と、**その上で動くアプリ**を管理するモノレポ。

## 構成

| Directory | 内容 |
|---|---|
| [`rom/`](rom/README.md) | ROM (Kiosk Satellite Edition) のビルド・成果物管理 |
| [`app/`](app/README.md) | Echo5 上で動作する Android アプリ |

## ビルド / リリース方針

- **ビルドは GitHub Actions に任せる** (ローカルに AOSP ツリーは置かない)
- **成果物は常に rolling prerelease `checkers-latest` のみ** (正式リリースは作らない)
- Actions のアーティファクトと prerelease にだけ成果物を残す

## ライセンス

MIT
