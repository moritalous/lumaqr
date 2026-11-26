# lumaqr

LumaのダークモードQR（白黒反転）が受付スキャナで読み取りにくい問題への対策ツールです。

- `site/scan.html` : 反転対応スキャナ。ライト／ダーク両方のQRを読み取り、チェックインURLを開きます（jsQR `attemptBoth`）。
- `site/mirror.html` : 反転ミラー。中継スマホで参加者の画面を撮影し、白黒反転して表示します。受付側はその画面を読み取ります。

カメラ映像は端末内でのみ処理され、外部へ送信されません。

## 公開（GitHub Pages）

リポジトリの Settings → Pages → Source を「GitHub Actions」に設定し、`main` へマージすると `.github/workflows/pages.yml` が `site/` を公開します。カメラ利用にはHTTPSが必要です。

`site/jsQR.js` は [jsQR](https://github.com/cozmo/jsQR) 1.4.0（Apache-2.0）をそのまま同梱しています。
