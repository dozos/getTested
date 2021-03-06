# Команды Git #

## Сохранить в репозитории ##

Назначение | Команда
-----------|--------
Создать репозиторий | PS D:\Project\Html\gitTester> **git init**
Добавить к репозиторию все файлы в каталоге | PS D:\Project\Html\gitTester> **git add .**
Добавить к репозиторию один файл | PS D:\Project\Html\gitTester> **git add** "_index.html_"
Сохранить файлы в репозитории с коментариями | PS D:\Project\Html\gitTester> **git commit -m** "_first commit_"
Указываем на удаленный репозиторий в облаке с коротким имененм **origin** | PS D:\Project\Html\gitTester> **git remote add origin https://github.com/dozos/getTested.git**
Сохраняем локальный репозиторий в облачный с коротким именем **origin** | PS D:\Project\Html\gitTester> **git push -u origin master** 
Загружаем изменения в локальный репозиторий из облачного | PS D:\Project\Html\gitTester> **git pull** 

## Извлечь из репозитория ##

Назначение | Команда
-----------|--------
Сделать клон репозитория из GitHub | PS D:\Project\Html\gitTester> **git clone https://github.com/dozos/getTested.git**

## Дополнительные команды ##

Назначение | Команда
-----------|--------
Статус локального ранилища | PS D:\Project\Html\gitTester> **git status**

## Команды VSCode ##

Назначение | Команда
-----------|--------
**МЕНЮ: Система управления версиями Git.**|
"Синхронизировать"                        | 
"Галочка"  | **Работа с локальным репозиторием**<br>**git add** "_index.html_"<br>**git commit -m** "_first commit_"<br>------------------<br>--> Показать вывод команд git<br>git add -A -- .<br>git commit --quiet --allow-empty-message --file - --all<br>git status -z -u<br>git symbolic-ref --short HEAD<br>git rev-parse master<br>git rev-parse --symbolic-full-name master@{u}<br>git rev-list --left-right master...refs/remotes/origin/master<br>git for-each-ref --format %(refname) %(objectname) --sort -committerdate<br>git remote --verbose<br>git show :doc/gitCommand.md<br>
------------------                        | 
========================================= |
**ВЫПАДАЮЩЕЕ МЕНЮ: Дополнительные действия.**|
"Загрузить с..."                          | 
"Отправить"                               | **git push**
"Отправить в:"                            | 
"Получить"                                | **git pull**
"Получить (переместить изменения из одной ветви в другую)" | 
"Синхронизация"                           | 
----------------------------------------- | ------------
"Опубликовать ветвь"                      | 
----------------------------------------- | ------------
"Зафиксировать все"                       | 
"Зафиксировать все (завершено)"           |  
"Зафиксировать все (изменения)"           | 
"Отменить последний комит"                | 
"Сделать комит из индекса"                | 
"Сделать комит из индекса (исправить)"    | 
"Сделать комит из индекса (с одобрением)" | 
----------------------------------------- | ------------
"Индексировать все изменения"             | 
"Отменить все изменения"                  | 
"Отменить индексацию всех изменений"      | 
----------------------------------------- | ------------
"Извлечь последнее спрятанное"            | 
"Извлечь спрятанное"                      | 
"Применить последнее спрятанное"          | 
"Применить спрятанное..."                 | 
"Спрятать"                                | 
"Спрятать (включить неотслеживаемые)"     | 
----------------------------------------- | ------------
"Показать вывод команд git"               | 
========================================= | ============
**СТРОКА СТАТУСА.**                       |
"master"                                  | Текущая ветка в репозитории
"О хх(стрелка вверх) yy(стрелка вниз)"    | nn - количество комитов которы нужно забрать из облачного репозитория<br>yy - количество комитов которые нужно выгрузить в облачный репозиторий<br>При нажатии: Фиксация в ветке "origin/master" загружает и выгружает комиты.<br>> git pull --tags origin master<br>From https://github.com/dozos/getTested<br> * branch            master     -> FETCH_HEAD<br>> git push origin master:master<br>> git show :doc/gitCommand.md<br>To https://github.com/dozos/getTested.git<br>   2bfcdd1..9a444ca  master -> master<br>> git status -z -u<br>> git symbolic-ref --short HEAD<br>> git rev-parse master<br>> git rev-parse --symbolic-full-name master@{u}<br>> git rev-list --left-right master...refs/remotes/origin/master<br>> git for-each-ref --format %(refname) %(objectname) --sort -committerdate<br>> git remote --verbose<br>> git show :doc/gitCommand.md


## Пользовательские алиасы ##

_файл: c:\Users\Dozos\.gitconfig_

Добавить секцию

    [alias]
        s = status --short
        st = status
        l = log --oneline --graph --decorate --all
        g = log --graph --abbrev-commit --decorate --all --format=format:'%C(bold blue)%h%C(reset) - %C(bold cyan)%aD%C(dim white) - %an%C(reset) %C(bold green)(%ar)%C(reset)%C(bold yellow)%d%C(reset)%n %C(white)%s%C(reset)'
        br = branch
        co = checkout
        