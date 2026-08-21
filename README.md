# ZMK config for Crosses

## 日本語キーボード設定

OS のハードウェアキーボードレイアウトを「日本語キーボード
(106/109 キー)」にしたまま使えるよう、`config/crosses.keymap` の記号キーを
JIS 配列向けの HID キーコードへ変換しています。

- 記号レイヤーでは `"`, `'`, `&`, `@`, `+`, `:`, `*`, `(`, `)`, `=`,
  `~`, `_`, `|` などを、JIS 設定時にも意図した記号として入力できます。
- `¥` と `_` には ZMK の `INTERNATIONAL_3` / `INTERNATIONAL_1` を使用します。
- 左親指キーはタップで `英数` (`LANGUAGE_2`) と `F24` を送信し、
  ホールドで `LCTRL` として動作します。
- 右親指キーはタップで `かな` (`LANGUAGE_1`) と `F23` を送信し、
  ホールドでレイヤー2を有効にします。

### Moonlight 経由のIME切り替え

通常接続では `LANGUAGE_1/2` がIMEを切り替え、追加の `F23/F24` は通常何も
起こしません。Moonlight経由では、リモートホスト側のAutoHotkeyなどで
`F23` をIME ON、`F24` をIME OFFへ割り当ててください。これにより、
通常接続とMoonlight経由で同じ親指操作を使えます。

Windows の日本語キーボード設定を前提にした方式です。macOS や Linux では
入力ソースや IME によって挙動が異なる場合があります。また、プリプロセッサの
独自定義を使うため、キーマップの変更は Keymap Editor や ZMK Studio ではなく、
`config/crosses.keymap` を直接編集してください。
