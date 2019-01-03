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


## Извлечь из репозитория ##

Назначение | Команда
-----------|--------
Сделать клон репозитория из GitHub | PS D:\Project\Html\gitTester> **git clone https://github.com/dozos/getTested.git**


## Дополнительные команды ##

Назначение | Команда
-----------|--------
Статус локального ранилища | PS D:\Project\Html\gitTester> **git status**