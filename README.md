# Домашнее задание к занятию 4. «PostgreSQL» - Сергей Ситкарёв

## Задача 1

Используя Docker, поднимите инстанс PostgreSQL (версию 13). Данные БД сохраните в volume.

Подключитесь к БД PostgreSQL, используя psql.

Воспользуйтесь командой \? для вывода подсказки по имеющимся в psql управляющим командам.

Найдите и приведите управляющие команды для:

вывода списка БД, - \l

подключения к БД, - \c db_name

вывода списка таблиц, - \dt

вывода описания содержимого таблиц, - \d[S+]

выхода из psql. - \q

## Задача 2

Используя psql, создайте БД test_database.

![Задание2](https://github.com/SSitkarev/06-db-04-postgresql/blob/main/img/2-1.jpg)

Изучите бэкап БД.

Восстановите бэкап БД в test_database.

![Задание2](https://github.com/SSitkarev/06-db-04-postgresql/blob/main/img/2-2.jpg)

Перейдите в управляющую консоль psql внутри контейнера.

Подключитесь к восстановленной БД и проведите операцию ANALYZE для сбора статистики по таблице.

![Задание2](https://github.com/SSitkarev/06-db-04-postgresql/blob/main/img/2-3.jpg)

Используя таблицу pg_stats, найдите столбец таблицы orders с наибольшим средним значением размера элементов в байтах.

![Задание2](https://github.com/SSitkarev/06-db-04-postgresql/blob/main/img/2-4.jpg)

## Задача 3

Архитектор и администратор БД выяснили, что ваша таблица orders разрослась до невиданных размеров и поиск по ней занимает долгое время. Вам как успешному выпускнику курсов DevOps в Нетологии предложили провести разбиение таблицы на 2: шардировать на orders_1 - price>499 и orders_2 - price<=499.

Предложите SQL-транзакцию для проведения этой операции.

![Задание3](https://github.com/SSitkarev/06-db-04-postgresql/blob/main/img/3.jpg)

Можно ли было изначально исключить ручное разбиение при проектировании таблицы orders? - Можно было создать таблицу секционированной.

## Задача 4

Используя утилиту pg_dump, создайте бекап БД test_database.

![Задание4](https://github.com/SSitkarev/06-db-04-postgresql/blob/main/img/4-1.jpg)

Как бы вы доработали бэкап-файл, чтобы добавить уникальность значения столбца title для таблиц test_database?

![Задание4](https://github.com/SSitkarev/06-db-04-postgresql/blob/main/img/4-2.jpg)