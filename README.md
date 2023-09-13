
# Приложение для просмотра расписания колледжа
Это приложение позволяет просматривать и использовать расписание занятий в колледже.

## Ключевые компоненты
- База данных SQLite, в которой хранится расписание в виде таблиц.
- Backend на Python с использованием фреймворка Flask.
  - Обрабатывает запросы от клиента
  - Делает выборку расписания из БД
  - Конвертирует данные в JSON
- Мобильное приложение на Android в качестве клиента
  - Делает запросы к backend по HTTP
  - Получает данные расписания в JSON формате
  - Отображает их в виде удобного для пользователя интерфейса

## Принцип работы
1. Изначально расписание заполняется в БД SQLite в виде связанных таблиц.
2. Приложение на Android делает HTTP запрос к бекенду (Flask) для получения данных.
3. Backend обрабатывает запрос, делает выборку нужных данных из БД, конвертирует результат в JSON.
4. JSON ответ отправляется приложению.
5. Код приложения на Android получает JSON, парсит его и отображает пользователю нужную информацию из расписания в удобном виде с использованием интерфейса Android.
6. При необходимости отправляются новые запросы для обновления данных.
