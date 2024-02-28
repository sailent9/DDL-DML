# DDL-DML Тихун Вадим 


### Задание 1
1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.

1.2. Создайте учётную запись sys_temp. 

```
CREATE USER 'sys_temp'@'localhost' IDENTIFIED BY 'temp';
```

1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)


![1 3](https://github.com/sailent9/DDL-DML/assets/130309754/e247667f-f1e0-4b85-8ddc-57e3247faade)

1.4. Дайте все права для пользователя sys_temp. 

```
GRANT ALL PRIVILEGES ON *.* TO 'sys_temp'@'localhost' WITH GRANT OPTION;
FLUSH PRIVILEGES;
```

1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)


![1 5](https://github.com/sailent9/DDL-DML/assets/130309754/f3a9e8e9-3665-4920-b0eb-0b179e31134f)

1.6. Переподключитесь к базе данных от имени sys_temp.

Для смены типа аутентификации с sha2 используйте запрос: 
```sql
ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```
1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.

1.7. Восстановите дамп в базу данных.

```
SOURCE /home/Vadik/sakila-db/sakila-schema.sql
SOURCE /home/Vadil/sakila-db/sakila-data.sql
```

1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)
![1 8](https://github.com/sailent9/DDL-DML/assets/130309754/80d7ebed-3fd9-4481-bcd6-08d928ab0bad)
![1 8 2](https://github.com/sailent9/DDL-DML/assets/130309754/029d4d13-1328-48f0-9a40-54c3831878d1)



*Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.*


### Задание 2
Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц. Пример: (скриншот/текст)
```
Название таблицы | Название первичного ключа
actor            | actor_id
address          | address_id
category         | category_id
city             | city_id
country          | country_id
customer         | customer_id
film             | film_id
film_actor       | actor_id, film_id
film_category    | film_id, category_id
film_text        | film_id
inventory        | inventory_id
language         | language_id
payment          | payment_id
rental           | rental_id
store            | store_id
staff            | staff_id
```
