# SHELL EMULATOR #

Разработать эмулятор для языка оболочки ОС. Необходимо сделать
работу эмулятора как можно более похожей на сеанс shell в UNIX-подобной ОС.
Эмулятор должен запускаться из реальной командной строки, а файл с
виртуальной файловой системой не нужно распаковывать у пользователя.
Эмулятор принимает образ виртуальной файловой системы в виде файла формата
tar. Эмулятор должен работать в режиме CLI.

**1. ОБЩЕЕ ОПИСАНИЕ.**

Этот проект представляет собой эмулятор командной строки, реализованный на
Python, который позволяет пользователю выполнять базовые команды файловой
системы, такие как ls, cd, du, и find. Эмулятор работает с виртуальной файловой
системой, распакованной из архива .tar, и сохраняет журнал действий в формате
JSON. Также включены тесты для проверки правильности работы функций
эмулятора.

**2. ОПИСАНИЕ ВСЕХ ФУНКЦИЙ И НАСТРОЕК**

Основные функции:

```handle_ls()``` :  Отображает список файлов и каталогов в текущем каталоге.

```handle_cd(path)``` : Переходит в указанный каталог.

```handle_exit()``` : Завершает работу эмулятора.

```handle_who()``` : Отображает информацию о пользователе и текущем хосте.

```handle_du()``` : Отображает использование дискового пространства для файлов в
текущем каталоге.

```handle_find(filename)``` : Ищет указанный файл в файловой системе.


Настройки:

```--user <имя пользователя>``` — Устанавливает имя пользователя, которое будет
отображаться в командной строке

```--host <имя хоста>``` — Устанавливает имя хоста.

```--fs <архив файловой системы>``` — Путь к архиву виртуальной файловой системы,
который нужно распаковать.

```--log <файл журнала>``` — Путь к файлу журнала, в котором сохраняются действия
пользователя.


**3. ОПИСАНИЕ КОМАНД ДЛЯ СБОРКИ ПРОЕКТА**

Для запуска эмулятора используется эта команда: 

```python shell_emulator.py --user <имя пользователя> --host <имя хоста> --fs <архив файловой системы> --log <файл журнала>```

Пример команды:

**python shell_emulator.py --user student --host localhost --fs virtual_fs.tar --log actions_log.json**


Для запуска тестов используется команда:

```python -m pytest```

**4. ПРИМЕРЫ ИСПОЛЬЗОВАНИЯ:**


```ls``` :

![image.png](images/image.png)

```cd``` : 

![image-1.png](images/image-1.png)

```who``` : 

![image-2.png](images/image-2.png)


```du``` : 

![image-3.png](images/image-3.png)


```find``` : 

![image-4.png](images/image-4.png)


```exit``` :

![image-5.png](images/image-5.png)

**5. РЕЗУЛЬТАТЫ ПРОГОНА ТЕСТОВ:**

![image-6.png](images/image-6.png)