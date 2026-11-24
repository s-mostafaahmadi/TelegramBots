# TelegramBots

Zwei kleine Telegram-Bots in Python, die meinen Windows-Desktop per Chat steuern bzw. beim Deutschlernen helfen. Beide Bots laufen lokal und nutzen `pyTelegramBotAPI` (`telebot`).

## Bots

### `tah3in_bot` – Desktop-Fernsteuerung

- Nimmt Links per Telegram an und startet den Download über den Internet Download Manager (`Open_IDM.py`).
- Arbeitet mit dem Desktop über `pyautogui` und `subprocess` (z. B. Dateien und Ordner öffnen).
- Merkt sich den Zustand pro Chat (`user_states`), damit mehrstufige Befehle funktionieren.
- Einstiegspunkt: `tah3in_bot.py`

### `deutsch_bot` – Vokabel- und Satztrainer

- Liest Wort- und Satzlisten aus `Wordlist.txt` und `Sentencelist.txt`.
- Fragt Wörter bzw. Sätze ab und schreibt neue Einträge zurück in die Liste (`replace_line_in_file`).
- Einstiegspunkt: `deutsch_bot.py`

## Einrichtung

1. Bot-Token bei [@BotFather](https://t.me/BotFather) erstellen und in beiden Dateien bei `BOT_TOKEN = ...` eintragen. Das Token gehört **nicht** ins Repository.
2. Abhängigkeiten installieren:

   ```bash
   pip install pyTelegramBotAPI pyautogui
   ```

3. Bot starten, jeweils im eigenen Ordner:

   ```bash
   cd tah3in_bot
   python tah3in_bot.py
   ```

   ```bash
   cd deutsch_bot
   python deutsch_bot.py
   ```

## Voraussetzungen

- Windows (Desktop-Steuerung und IDM-Anbindung sind Windows-spezifisch)
- Python 3.10+
- Internet Download Manager für `Open_IDM.py`
