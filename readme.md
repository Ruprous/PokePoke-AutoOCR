# ポケポケ支援ツールセット（Pokemon TCG Pocket Tools）

このリポジトリは、ポケポケ（Pokemon TCG Pocket）プレイヤー向けの支援ツールセットです。OBS配信や自動記録をサポートするためのPythonスクリプトを含んでいます。

---

## 📁 同梱ツール

### `poke_auto.py`（ポケポケ自動情報取得）

- **対応環境**：Windows＋Androidエミュレータ（BlueStacks, NOXなど）
- **主な機能**：
  - 相手の名前をOCRで取得（Pキー）
  - 試合中の持ち時間をOCRで自動取得
  - 点数状態の取得（色判定）

- **出力ファイル**（OBSなどで表示に使える）：
  - `player_info.txt`
  - `opponent_info.txt`
  - `self_signal_status.txt`
  - `opponent_signal_status.txt`

- **必要ライブラリ**：
  ```bash
  pip install pytesseract pillow keyboard
  ```

- **Tesseract OCRの導入も必要**  
  https://github.com/tesseract-ocr/tesseract

---

### `cursor_auto.py`（マウス座標キャプチャ）

- **概要**：マウスの現在位置を1秒ごとに表示
- **使い方**：
  ```bash
  pip install pyautogui
  python cursor_auto.py
  ```
  `Ctrl+C`で終了できます。

---

## 🧠 注意

- スクリプトは **1920x1080の解像度** を前提に設計されているため、必要に応じて座標を調整してください。
- `poke_auto.py` のOCRがうまく動作しない場合は、Tesseractの設定やフォント・画面拡大率を見直してみてください。

