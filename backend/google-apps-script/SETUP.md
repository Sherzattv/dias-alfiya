# Настройка Google Sheets + Telegram для RSVP

## 1) Создайте Google Sheet
- Создайте новую таблицу в Google Sheets.
- Скопируйте `ID` таблицы из URL:
  `https://docs.google.com/spreadsheets/d/<SPREADSHEET_ID>/edit`

## 2) Создайте Apps Script Web App
- Откройте [script.google.com](https://script.google.com) и создайте новый проект.
- Вставьте код из файла [`Code.gs`](/Users/sherzat/wedding_page/backend/google-apps-script/Code.gs).
- В `Project Settings` откройте `Script properties` и добавьте:
  - `SPREADSHEET_ID` = ID вашей таблицы
  - `SHEET_NAME` = `RSVP` (или любое название листа)
  - `TELEGRAM_BOT_TOKEN` = токен бота
  - `TELEGRAM_CHAT_ID` = id чата/группы для уведомлений

## 3) Деплой
- `Deploy` -> `New deployment` -> тип `Web app`.
- `Execute as`: `Me`.
- `Who has access`: `Anyone`.
- Нажмите `Deploy` и скопируйте URL вида:
  `https://script.google.com/macros/s/.../exec`

## 4) Подключите URL в сайте
- Откройте [`index.html`](/Users/sherzat/wedding_page/index.html).
- Найдите строку:
  `const RSVP_ENDPOINT = "";`
- Вставьте URL веб‑приложения:
  `const RSVP_ENDPOINT = "https://script.google.com/macros/s/.../exec";`

## 5) Проверка
- Нажмите на сайте «Буду с радостью», заполните форму и отправьте.
- Должно произойти:
  - новая строка в листе `RSVP`
  - сообщение в Telegram о новой заявке
