# PokePoke Support Toolset (Pokemon TCG Pocket Tools)

This repository contains support tools for players of **Pokemon TCG Pocket (PokePoke)**.  
It includes Python scripts designed to help with streaming via OBS and automatic game data tracking.

---

## 📁 Included Tools

### `poke_auto.py` (Automatic Info Capture Tool)

- **Environment**: Windows + Android emulator (BlueStacks, NOX, etc.)
- **Main Features**:
  - OCR-based opponent name capture (press `P` key)
  - Automatic time tracking for both players
  - Score status detection based on color checking

- **Output Files** (for OBS text overlay):
  - `player_info.txt`
  - `opponent_info.txt`
  - `self_signal_status.txt`
  - `opponent_signal_status.txt`

- **Required Libraries**:
  ```bash
  pip install pytesseract pillow keyboard
  ```

- **Tesseract OCR must be installed**  
  https://github.com/tesseract-ocr/tesseract

---

### `cursor_auto.py` (Mouse Position Capturer)

- **Description**: Displays the current mouse position every second.
- **How to use**:
  ```bash
  pip install pyautogui
  python cursor_auto.py
  ```
  Stop with `Ctrl+C`.

---

## 🧠 Notes

- Scripts are designed for **1920x1080 resolution**.  
  Please adjust coordinate settings if using a different resolution.
- If `poke_auto.py` doesn't capture text correctly, check your Tesseract path and screen scaling.

