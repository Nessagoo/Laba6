# Лабораторная работа №6: Уведомления и напоминания в Android

## Описание.
Это приложение предоставляет пользователю возможность создавать напоминания с заголовком, текстом и датой, которые сохраняются в базу данных и отображаются в виде уведомлений. Напоминания можно просматривать, удалять, а также они отображаются в статус-баре с пользовательской иконкой. При нажатии на уведомление происходит переход к активности с полным описанием напоминания.

## Основные функции

1. **Создание напоминаний и сохранение в базу данных**: Пользователь может создать напоминание с заголовком, текстом и датой. Эти данные сохраняются в базу данных.
2. **Просмотр напоминаний**: Отдельный экран отображает список всех созданных напоминаний.
3. **Удаление напоминаний**: Пользователь может удалить любое напоминание, нажав на него в списке.
4. **Установка уведомления с помощью AlarmManager**: Уведомление для напоминания настраивается с использованием `AlarmManager`, `PendingIntent` и `BroadcastReceiver`.
5. **Уведомления с переходом в активность**: При нажатии на уведомление открывается экран с полной информацией о напоминании.

## Структура приложения

Приложение состоит из нескольких основных экранов и классов для работы с уведомлениями и базой данных:

1. **MainActivity**:
   - **Описание**: Основной экран приложения, на котором пользователь вводит заголовок, текст напоминания и выбирает дату/время.
   - **Кнопки**:
     - **Сохранить напоминание**: Добавляет новое напоминание в базу данных и устанавливает уведомление.
     - **Просмотреть напоминания**: Переход на экран со списком всех созданных напоминаний.

2. **ReminderListActivity**:
   - **Описание**: Экран, отображающий список всех напоминаний из базы данных.
   - **Элементы**:
     - **RecyclerView**: Список напоминаний с заголовками, датой и временем. Каждое напоминание имеет кнопку для удаления.

3. **ReminderDetailActivity**:
   - **Описание**: Экран, который отображает полную информацию о напоминании при нажатии на уведомление в статус-баре.
   - **Элементы**:
     - **TextView**: Показывает заголовок и текст напоминания.

4. **BroadcastReceiver**:
   - **Описание**: Обрабатывает срабатывание уведомления в нужное время и переход на экран с деталями напоминания.

## Внешний вид приложения

- **MainActivity**:
  - Поля для ввода заголовка и текста напоминания.
  - Кнопка для выбора даты и времени.
  - Кнопки для сохранения напоминания и просмотра списка.

- **ReminderListActivity**:
  - Список напоминаний с заголовками, датами, временем и кнопками для удаления.
