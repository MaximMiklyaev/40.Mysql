# MySQL(Centos 7)
----------------------------------------------------------------------- 

```
Домашнее задание
Развернуть базу из дампа и настроить репликацию
Цель: В результате выполнения ДЗ студент развернет базу из дампа и настроит репликацию.
В материалах приложены ссылки на вагрант для репликации
и дамп базы bet.dmp
базу развернуть на мастере
и настроить чтобы реплицировались таблицы
| bookmaker |
| competition |
| market |
| odds |
| outcome

* Настроить GTID репликацию

варианты которые принимаются к сдаче
- рабочий вагрантафайл
- скрины или логи SHOW TABLES
* конфиги
* пример в логе изменения строки и появления строки на реплике  
```

### Как запустить:
- git clone https://github.com/MaximMiklyaev/40.Mysql.git && cd 40.Mysql && vagrant up

### Описание:

1. После поднятия виртуальных машин, выполним операции на мастере:

![Image 1](https://raw.githubusercontent.com/MaximMiklyaev/40.Mysql/master/screenshots/master.png)

![Image 2](https://raw.githubusercontent.com/MaximMiklyaev/40.Mysql/master/screenshots/master2.png)

2. Посмотрим репликацию на slave:

![Image 3](https://raw.githubusercontent.com/MaximMiklyaev/40.Mysql/master/screenshots/slave.png)

![Image 4](https://raw.githubusercontent.com/MaximMiklyaev/40.Mysql/master/screenshots/slave2.png)

- Используем утилиту ```mysqlbinlog```:

![Image 5](https://raw.githubusercontent.com/MaximMiklyaev/40.Mysql/master/screenshots/binlog.png)

### Как проверить:

- Пароль для входа в mysql находиться в ```/home/vagrant/my.cnf```