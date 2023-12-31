# VK_farm
***
## Что это?
**VK_farm** - Проект, который поможет управлять большим количеством аккаунтов вконтакте. Создавал этот проект
для своих целей, по рассылке сообщений, но решил поделиться им с вами) 
## Какие задачи поможет решить?

1. Основная задача - массовая рассылка сообщений
2. Массовое рассылка приглашений в друзья
3. Создание и удаление постов
4. Рассылка постов
5. Смена аватарок
6. Проверка новых сообщений на аккаунтах и автоматический ответ на них
7. Вести учёт аккаунтов и сообщений в БД 

(Раньше ещё был рабочий авторег, но в вк изменили систему регистрации, что не позволяет ему работать.
Если у вас есть рабочее решение, свяжитесь со мной, добавлю его сюда)

## Как работать?

* Каждый файл и функция в нём, имеют описание. Следует с этим ознакомиться.
* После ознакомлением с функционалом, каждому аккаунту следует создать токен для работы с VK API. Это делается здесь: https://vkhost.github.io/.
* Нужно заполнить списки в [data.py](data.py), необходимые для работы. Списки содержат примеры и шаблоны правильного заполнения. Этого достаточно для работы без БД 
* Для работы с использованием БД, после успешного заполнения list_accounts в файле [data.py](data.py), нужно запустить функцию migration_accounts_to_db из [db_functions.py](db_functions.py).
* Для удобства, можно создать файлы для часто запускаемых функций и запускать их, либо же вызывать через терминал.

## Какие файлы за что отвечают?
* [data.py](data.py): Хранит списки с данными для работы.
* [db_creating.py](db_creating.py): Этот скрипт запускает функции создания таблиц для аккаунтов и сообщений.
* [db_executes.py](db_executes.py): Содержит команды для взаимодействия с БД
* [db_functions.py](db_functions.py): Здесь собраны все функции управления фермой аккаунтов, которые взаимодействуют с базой данных.
* [functions.py](functions.py): Содержит все функции управления фермой аккаунтов.
* [parsing_friends.py](parsing_friends.py): Парсер друзей пользователй.
* [parsing_groups.py](parsing_groups.py): Парсер участников сообществ.