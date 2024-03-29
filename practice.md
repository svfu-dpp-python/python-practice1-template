# Практическое задание 1

## Предварительные шаги

Перед выполнением задания склонируйте репозиторий на локальный компьютер:

```
cd <каталог для размещения проекта>
git clone <URL репозитория>
cd <каталог репозитория>
```

## Ход работы

1. Создайте пакет `package` и в нем вложенный пакет `sub_package` (не забудьте
   в каждом из них создать файл `__init__.py`).

   Внутри `sub_package` создайте модуль `my_module2.py`.

   В этом модуле напишите две функции: `weekday()` и `month()` без
   использования оператора ветвления `if`.

   Функция `weekday()` должна принимать одно целое положительное число в
   диапазоне от 1 до 7. Функция должна возвращать название дня недели на
   русском языке записанное строчными (маленькими) буквами (например
   `понедельник`).

   Функция `month()`, должна получать целое положительное число от 1 до 12.
   Функция должна возвращать название месяца на русском языке записанное
   строчными (маленькими) буквами в родительном падеже (например `января`,
   `февраля` и т.п.).

2. В пакет `package` создайте модуль `my_module1.py`

   В этот модуль импортируйте функции `weekday()` и `month()` из п.1 и класс
   `date` из модуля `datetime`.

   Ознакомьтесь с документацией по атрибутов `day`, `month`, `year` и метода
   `isoweekday()` у объектов класса
   [`datetime.date`](https://docs.python.org/3/library/datetime.html#date-objects).

   В этот модуль добавьте функцию `date_repr()` которая получает дату и
   возвращает строковое представление даты вида: `четверг 1 сентября 2022
   года`.

   Указание: [используйте форматные строки](https://pythonz.net/references/named/str-f/).

   В заголовок пакета `package` (файл `__init__.py`) добавьте импорт функции
   `date_repr()`.

3. В каталоге проекта создайте стартовый скрипт `start.py` и добавьте в него
   импорт функции `date_repr()` из заголовка пакета `package` и функции `date`
   из пакета `datetime` (он является частью стандартной библиотеки, см. выше).

   Добавьте в него код который запрашивает у пользователя дату с помощью
   функции `input()` (с показом запроса пользователю). Дату следует запросить в
   формате "ДД.ММ.ГГГГ" (например 01.09.2022).

   Далее код должен разбить введенную строку на компоненты и создать объект
   класса `datetime.date`.

   После этого код должен напечатать строковое представление, которое
   сформировано функцией `date_repr()`.

   Добавленный в `start.py` код не должен выполняться при его импортировании.

## Дополнительные ссылки

* Ознакомьтесь с документацией по объектам класса [`datetime.date`](https://docs.python.org/3/library/datetime.html#date-objects).
