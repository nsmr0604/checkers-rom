# checkers-rom

軽量スマートディスプレイ OS — Amazon Echo Show 5 (1st gen / codename **`checkers`**) 用。

## 概要

実機の Echo Show 5 (H23K37 / MT8163 / 32bit / RAM 1GB) を、
Home Assistant のキオスクダッシュボードとして必要十分に動作する Android 11 ROM に置き換える。

ベースは [jxlarrea/lineageos-echo-kiosk-satellite](https://github.com/jxlarrea/lineageos-echo-kiosk-satellite)
(R0rt1z2 氏の amazon-oss LineageOS 18.1 ポート + Kiosk Satellite Edition)。
不要アプリを削って 1GB RAM のうち約 400MB を空けた軽量構成。

## ビルド方針

- **ビルドは GitHub Actions に任せる** (ローカルに AOSP ツリーは置かない)
- **成果物は常に rolling prerelease `checkers-latest` のみ** (正式リリースは作らない)
- Actions のアーティファクトと prerelease にだけ成果物を残す

## 現状

- [x] リポジトリ作成
- [x] 軽量検証 workflow (`.github/workflows/validate.yml`) — Actions 発火・prerelease 添付の確認
- [ ] セルフホストランナー準備 (AOSP ビルドは 100GB 超のディスクと 32GB 以上の RAM が必要)
- [ ] `make checkers` 本番ビルド workflow 追加
- [ ] 実機 (TWRP 3.7.0_9-0) へ流し込み検証

## ライセンス

MIT
