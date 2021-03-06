<h2 align=center> Информационные системы и базы данных (лабораторные работы) </h2>
<h6 align=center> <a href="https://github.com/tolikttaaa/CourseProject_ISBD"> Информационные системы и базы данных (курсовой проект)</a> </h6>

<h3 align=center> <a href="Lab1">Лабораторная работа №1</a> </h3>

Для выполнения лабораторной работы №1 необходимо:

На основе предложенной предметной области (текста) составить ее описание. Из полученного описания выделить сущности, их атрибуты и связи.
Составить инфологическую модель.
Составить даталогическую модель. При описании типов данных для атрибутов должны использоваться типы из СУБД PostgreSQL.
Реализовать даталогическую модель в PostgreSQL. При описании и реализации даталогической модели должны учитываться ограничения целостности, которые характерны для полученной предметной области.
Заполнить созданные таблицы тестовыми данными.

<h3 align=center> <a href="Lab2">Лабораторная работа №2</a> </h3>

Составить запросы на языке SQL (пункты 1-7).

* Сделать запрос для получения атрибутов из указанных таблиц, применив фильтры по указанным условиям:

Таблицы: Н_ЛЮДИ, Н_СЕССИЯ. <br>
Вывести атрибуты: Н_ЛЮДИ.ИМЯ, Н_СЕССИЯ.ЧЛВК_ИД. <br>
Фильтры (AND): <br>
a) Н_ЛЮДИ.ИД < 100865. <br>
b) Н_СЕССИЯ.ЧЛВК_ИД > 100622. <br>
Вид соединения: INNER JOIN. <br>

* Сделать запрос для получения атрибутов из указанных таблиц, применив фильтры по указанным условиям:
Таблицы: Н_ЛЮДИ, Н_ОБУЧЕНИЯ, Н_УЧЕНИКИ.

* Вывести атрибуты: Н_ЛЮДИ.ОТЧЕСТВО, Н_ОБУЧЕНИЯ.ЧЛВК_ИД, Н_УЧЕНИКИ.ГРУППА.
Фильтры: (AND)

a) Н_ЛЮДИ.ОТЧЕСТВО < Владимирович. <br>
b) Н_ОБУЧЕНИЯ.ЧЛВК_ИД < 113409. <br>
c) Н_УЧЕНИКИ.ГРУППА > 5100. <br>
Вид соединения: INNER JOIN. <br>

* Вывести число студентов ФКТИУ, которые не имеет отчества. Ответ должен содержать только одно число.

* Найти группы, в которых в 2011 году было более 10 обучающихся студентов на ФКТИУ. Для реализации использовать соединение таблиц.

* Выведите таблицу со средними оценками студентов группы 4100 (Номер, ФИО, Ср_оценка), у которых средняя оценка больше минимальной оценк(е|и) в группе 1101.

* Получить список студентов, зачисленных ровно первого сентября 2012 года на первый курс очной формы обучения. В результат включить:

номер группы; <br>
номер, фамилию, имя и отчество студента; <br>
номер и состояние пункта приказа; <br>
Для реализации использовать подзапрос с EXISTS.

* Вывести список людей, не являющихся или не являвшихся студентами ФКТИУ (данные, о которых отсутствуют в таблице Н_УЧЕНИКИ). В запросе нельзя использовать DISTINCT.

<h3 align=center> <a href="Lab3/EMashina_Lab3.pdf">Лабораторная работа №3</a> </h3>

Составить запросы на языке SQL (пункты 1-2).

Для каждого запроса предложить индексы, добавление которых уменьшит время выполнения запроса (указать таблицы/атрибуты, для которых нужно добавить индексы, написать тип индекса; объяснить, почему добавление индекса будет полезным для данного запроса).

Для запросов 1-2 необходимо составить возможные планы выполнения запросов. Планы составляются на основании предположения, что в таблицах отсутствуют индексы. Из составленных планов необходимо выбрать оптимальный и объяснить свой выбор.
Изменятся ли планы при добавлении индекса и как?

Для запросов 1-2 необходимо добавить в отчет вывод команды EXPLAIN ANALYZE [запрос]

Подробные ответы на все вышеперечисленные вопросы должны присутствовать в отчете (планы выполнения запросов должны быть нарисованы, ответы на вопросы - представлены в текстовом виде).

* Сделать запрос для получения атрибутов из указанных таблиц, применив фильтры по указанным условиям:

Таблицы: Н_ЛЮДИ, Н_СЕССИЯ. <br>
Вывести атрибуты: Н_ЛЮДИ.ИД, Н_СЕССИЯ.ИД. <br>
Фильтры (AND): <br>
a) Н_ЛЮДИ.ИД = 142095. <br>
b) Н_СЕССИЯ.ИД > 14369. <br>
c) Н_СЕССИЯ.ИД = 14. <br>
Вид соединения: INNER JOIN. <br>

* Сделать запрос для получения атрибутов из указанных таблиц, применив фильтры по указанным условиям:

Таблицы: Н_ЛЮДИ, Н_ОБУЧЕНИЯ, Н_УЧЕНИКИ. <br>
Вывести атрибуты: Н_ЛЮДИ.ОТЧЕСТВО, Н_ОБУЧЕНИЯ.ЧЛВК_ИД, Н_УЧЕНИКИ.ГРУППА. <br>
Фильтры: (AND) <br>
a) Н_ЛЮДИ.ИМЯ = Ярослав. <br>
b) Н_ОБУЧЕНИЯ.НЗК = 933232. <br>
Вид соединения: INNER JOIN. <br>

<h3 align=center> <a href="Lab4">Лабораторная работа №4</a> </h3>

Для отношений, полученных при построении предметной области из лабораторной работы №1, выполните следующие действия:
* опишите функциональные зависимости для отношений полученной схемы (минимальное множество);
* приведите отношения в 3NF (как минимум). Постройте схему на основеNF (как минимум). Постройте схему на основе полученных отношений;
* опишите изменения в функциональных зависимостях, произошедшие после преобразования в 3NF (как минимум). Постройте схему на основеNF;
* преобразуйте отношения в BCNF. Докажите, что полученные отношения представлены в BCNF;
* какие денормализации будут полезны для вашей схемы? Приведите подробное описание.

