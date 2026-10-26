# Telegram NFT Bot

Бот для офферов NFT-подарков через Business Connection (команда `.buy`), подписки (TON / Stars) и админ-панель.

## Быстрый старт (одна кнопка)

### Windows
1. Открой папку `telegram_nft_bot`
2. Дважды кликни **`start.bat`**
3. При первом запуске откроется `.env` — вставь токен от [@BotFather](https://t.me/BotFather) в `BOT_TOKEN=...` и сохрани
4. Снова запусти **`start.bat`**

### Linux / macOS
```bash
chmod +x start.sh
./start.sh
```
При первом запуске создастся `.env` — укажи `BOT_TOKEN` и запусти снова.

## Настройка

Файл `.env` (рядом с `bot.py`):

| Переменная | Описание |
|---|---|
| `BOT_TOKEN` | Токен бота (обязательно) |
| `ADMIN_ID` | Твой Telegram ID для `/admin` |
| `TON_ADDRESS` | Адрес кошелька для оплаты подписки |
| `TONCENTER_API_KEY` | Опционально, ключ [toncenter.com](https://toncenter.com) |
| `SUBSCRIPTION_PRICE_TON` | Цена по умолчанию (TON) |
| `SUBSCRIPTION_DAYS` | Срок подписки по умолчанию |

База данных: `data/access.db` (создаётся автоматически).

## Команды

- `/start` — панель / покупка подписки
- `/menu` или `/panel` — панель пользователя (нужен доступ)
- `/admin` — админ-панель (только `ADMIN_ID`)
- В бизнес-чате: `.buy https://t.me/nft/Name-123 150 stars ru`

## Важно

- Токен **не** хранится в коде — только в `.env`
- Не публикуй `.env` и папку `data/`
- Для Business Messages бот должен быть подключён как Telegram Business бот у аккаунта-продавца
