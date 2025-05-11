# Military Aircraft Tracker 🇸🇰

Skript na sledovanie vojenských lietadiel podľa callsignu cez tar1090 a odosielanie správ do Telegramu spolu s mapou z LocationIQ (OSM).

## ✅ Závislosti
- Python 3 + virtualenv
- Knižnice: `requests`, `pillow`

## 📦 Inštalácia

1. Vytvor virtualenv:
   ```bash
   python3 -m venv ~/m
   source ~/m/bin/activate
   pip install -r requirements.txt
   ```

2. Uprav v skripte:
   - `TELEGRAM_TOKEN`
   - `TELEGRAM_CHAT_ID`
   - `LOCATIONIQ_TOKEN`

3. Umiestni službu:
   ```bash
   sudo cp mil-air.service /etc/systemd/system/
   sudo systemctl daemon-reload
   sudo systemctl enable mil-air.service
   sudo systemctl start mil-air.service
   ```

## 🛠️ Sledovanie logu služby
```bash
journalctl -u mil-air.service -f
```

## 🔗 Služby
- Telegram Bot: https://t.me/BotFather
- LocationIQ API: https://locationiq.com