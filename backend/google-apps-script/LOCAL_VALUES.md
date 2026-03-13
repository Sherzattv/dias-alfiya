# Ваши значения (подстановка)

## Script Properties в Google Apps Script
- `SPREADSHEET_ID` = `1bzIP8Yxvpy8tbadqV5QXCZ7ltDWzLG2o0qnTPbpxGzY`
- `SHEET_NAME` = `RSVP`
- `TELEGRAM_BOT_TOKEN` = `8492436207:AAGeyJ5LP_HQwmDyvTt2TMy2R_LoSDGQ7nE`
- `TELEGRAM_CHAT_ID` = `-5115133023`

## В index.html
Найдите:
```js
const RSVP_ENDPOINT = "";
```
И вставьте URL вашего Apps Script Web App (после Deploy):
```js
const RSVP_ENDPOINT = "https://script.google.com/macros/s/XXXX/exec";
```
