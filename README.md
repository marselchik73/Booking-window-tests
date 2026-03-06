# Booking Window Tests

Тесты для API окна бронирования (поля: имя, email, телефон).
Окно бронирования доступно по ссылке: [marselchik73.github.io/Booking-window](https://marselchik73.github.io/Booking-window/)

## Эндпоинт для тестирования
- URL: `https://jsonplaceholder.typicode.com/posts`
- Метод: `POST`
- Заголовки: `Content-Type: application/json`
- Тело запроса (пример):
  ```json
  {
    "name": "Иван Петров",
    "email": "ivan@example.com",
    "phone": "89991234567"
  }

**Важно:**  
Тесты написаны в расчёте на реальное API с валидацией данных.  
В данный момент используется тестовый бэкенд (jsonplaceholder), 
который не проверяет корректность полей, поэтому некоторые тесты могут вести себя иначе, 
чем на реальном сервере.

## Коллекции Postman

В папке `postman` находятся следующие коллекции:

- `Booking_Window_Positive.json` - позитивные тесты (ручные)
- `Booking_Window_Positive_Auto.json` - позитивные тесты (автоматизированные)
- `Booking_Window_Negative.json` - негативные тесты (ручные)
- `Booking_Window_Negative_Auto.json` - негативные тесты (автоматизированные)

## Запуск тестов

### В Postman

Импортируйте нужные коллекции через **File → Import**:
- `Booking_Window_Positive.json` - позитивные сценарии (ручная проверка)
- `Booking_Window_Negative.json` - негативные сценарии (ручная проверка)
- `Booking_Window_Positive_Auto.json` - позитивные сценарии с автотестами
- `Booking_Window_Negative_Auto.json` - негативные сценарии с автотестами


### Из командной строки (Newman)

```bash
newman run postman/Booking_Window_Positive_Auto.json
newman run postman/Booking_Window_Negative_Auto.json


