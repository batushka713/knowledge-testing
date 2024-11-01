# Инструкция по языку MarkDown и Контролю версий Git
## Подсказка по Git
* *Создания репозитория*
```sh
git init
```
* *Добавления файла*
```sh
git add
```
* *Добавление комментария к изменениям*
```sh
git commit -m "Message"
```
* *Просмотр коментариев к файлам*
```sh
git log
```
* *Просмотр коментариев к файлам скороткими ссылками*
```sh
git log --oneline
```
* *Переход к другой версии*
```sh
git checkout <branch_name> 
```
* *Переход к веткам файла*
```sh
git checkout master
```
* *Команда для смены директории Linux,MacOs*
```sh
cd c:\folder_name
```
* *Команда для смены директории Windows*
```sh
cd c:\User\Uzer_Name\Desktop\Folder_Name
```
* *Команда отображения текущей директории.MacOs,Linux*
```sh
pwd
```
* *Листинг текущей директории Windows*
```sh
dir
```
* *Linux, MacOs*
```sh
ls
```
* *Удаление файла Windows* 
```sh
del <filename>
```
* *В linux,MacOs*
```sh
rm <filename>
```
просмотр всех веток
```sh
git branch
```
Создание новой ветки
```sh
git branch <branch_name>    
```
Удаление веток
```sh
git branch -d <branch_name>
```
Вывидение графиков комитов
```sh
git lod --graph
```
Слияние двух веток
```sh
git marge 
```
Для просмотра подготовленных изменений необходимо добавить флаг --staged.

```sh
git diff --staged
```
Переименовать файл или папку можно параметром mv. Для него указывается источник source и назначение destination. Источник — реально существующий файл или папка, а назначение — существующая папка.
```sh
git mv dir1/somefile.js dir2
```
Внести изменения в последний коммит можно параметром commit с флагом --amend. Например, вы записали изменения, внесённые в ряд файлов, и поняли, что допустили ошибку в сообщении коммита. В этом случае можете воспользоваться указанной командой, чтобы отредактировать сообщение предыдущего коммита, не изменяя его снимок.
```sh
git commit --amend -m "Updated message for the previous commit"
```
Удаление файла происходит чере флаг -d
```sh
git branch -d <branch_name>
```
## Команды для создания ssh Ключей и агентов

"Для github индкс при создании ключа должен быть ed25519"

Команда для создания ssh ключа
```sh
ssh-keygen -t ed25519  -C <Если нужен коментариий, принличие нескольких ключей>
```
Команда для создания Ssh Агента 
```sh
evel "$(ssh-agent -s)"
```
Команда для привязки агента к ключу
```sh
ssh-add ~/.ssh/id_ed25519
```
[Информация по добовлению ключей Ssh](https://stackoverflow.com/questions/35901982/how-do-i-add-an-ssh-key-in-gitlab "Ссылка на статью Gitlab" )

[подробная статья про Ssh](https://best-manual.ru/blog/diy/2022-11-21-nastrojka-dostupa-po-ssh-klyuchu-v-github-v-windows-i-macos.html)

## Команды для работы с удаленными репазиториями
Команда для подключение удоленного репазитория к локальному 
```sh
git remote add origin<Ssh код удоленного репазитория>
```
команда для получения файлов с удаленного репазитория
```sh
git push <Ssh код удоленного репазитория>
```
Или
```sh
git clone <Ssh код удоленного репазитория>
```
Команда для отправки файлов на удаленный репазиторий
```sh
git push
```
## Оформление текста в MarkDown
Чтобы текст начинался с новой строки нужно два отступа

**Полужирный текст**

*Курсив*

## Цитирование в MarkDown
>Первый уровень цитирование
>>Второй уровень 
>>>Третий уровень 

## Списки 
### Нумеровоный список 
1.Лист
2.Лист
### Не нумеровоный список
* Лист 1
* Лист 2

### Вложеный список
1.пример
     
     1.пример

### Добавление картинок
![Изоброжение](https://is1-ssl.mzstatic.com/image/thumb/Purple113/v4/5d/0f/94/5d0f9492-b1fe-08de-9861-ff963e663625/AppIcon-0-85-220-4-2x.png/1200x630bb.png "Логотип MarkDown")

## Web Ссылки
[Статья на Википедии](https://ru.wikipedia.org/wiki/Markdown " облегчённый язык разметки")
