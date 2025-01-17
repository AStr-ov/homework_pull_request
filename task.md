Дополнить файл с инструкцией по работе с git (второе домашнее задание) и направить pull request в этот репозиторий. Файл с инструкцией необходимо дополнить информацией о работе с удаленными репозиториями.

В системе подгрузить скриншот отправленного pull request


# Инструкция по работе с git репозиторием

## Для начала работы:
__git init__ - создает пустой репозиторий, в которм будут храниться дальнейшие изменения - коммиты

Если имя пользователя и почта еще не были заданы:

* git config --global user.name  - прописываем свой ник
* git config --global user.email - прописываем адрес электронной почты

## Работа с файлами:
*Для того чтобы добавить файл, нужно:*
1. >__git add__ file_name -

   Добавляет файл с именем file_name для отслеживания (индексирует), после чего его можно коммитить.

   * >Вариант __git -A__ 

   добавляет все раннее проиндексированные файлы (т.е. уже отработанные коммандой *git add*).

   * >Вариант __git .__   
   
   добавляет все файлы в данной папке, включая новые
2. >**git commit -m** "some message"

   добавляет текущее изменение в репозиторий и подписывает
    их с помощью тега -m ("some message"- комментарий-название коммита).

   >**git commit -a** 

   совершит коммит, автоматически индексируя изменения в файлах т.е. комманда 

   **git commit -a** позволяет не вводить предворительно комманду **git add** 

 *Чтобы отслеживать состояние репозитория:*

1. > **git status** 

 показывает текущее состояние проекта

2. >**git log** 

 показывает существующие коммиты с уникальными кодами и подписанные комментариями

3. >**git diff**   

показывает только отличие после коммита

## Работа с коммитами
*Для того чтобы перейти к определенному коммиту
можно использовать команду* -

>**git checkout** code_commit

code_commit - код коммита, к которому хотим перейти, его можно посмотреть в __git log__


*Чтобы вернуться к самому последнему состоянию*:
>**git checkout master**

![здесь должна быть сова](sova.jpg)


 ## Ветки в git
 Чтобы посмотреть все ветки:
 >**git branch**

Для создания новой ветки с именем branch_name:

 >**git branch** branch_name


Переместиться к ветке с именем branch_name:
 > **git checkout** branch_name

 ## Слияние веток и решение конфликтов
 Чтобы слить информацию из ветки branch_name в текущую:
  >**git merge** branch_name

 В случае конфликта нужно удалить все лишние строки и оставить ту часть, которая нам нужна. Если необходимо, то можно отредактировать ее.

 ## Удаленеие веток
 Для того чтлбы удалить ветку с именем branch_name:
  >**git branch -d** branch_name

 Удаление с игнорированием ошибок:
  >**git branch -D** branch_name

  
##  Работа с удаленными репозиториями.

Для пользования удаленными репозиториями,
сперва необходимо пройти процедуру регистрации
на выбраном сервере.
## Копировать удаленный репозиторий 
можно командой:
> **git clone** <ссылка на удаленный репозиторий>

 ссылку можно скопировать на сервере, нажав **"Code"** на выбранном репозитории.


## Отправить локальный репозиторий на удаленный:
 
 1. *Подключаем удаленный репозиторий к локальному*:

 * >**git remote add origin** <ссылка на удаленный репозиторий>

ссылку можно скопировать на сервере, нажав **"Code"** на выбранном репозитории.

* >**git branch -M main**

* >**git push -u origin main**

 2. *Копируем содержимое локального репозитория на удаленный командой :*

  * > **git push**

 Получить обновленное содержание привязанного раннее удаленного репозитория на локальный можно командой 
> **git pull**

При этом автоматически произойдет и "сливание" репозиториев. Возможные конфликты надо устранить, редактируя файл вручную в любом редакторе. 

## Предложить свои изменения в чей-то репозиторий 

* Cкопировать его на свой удаленный репозиторий, нажав **Fork**,
* Работать со своей копией.
* На странице своей копии репозитория на GitHub нажать кнопку **Pull Request**.

 Далее можно сделать описание предлагаемых изменений.


  ## Справка
  Чтобы вызвать справку по команде допишите тег:
  >**--help**

  Примеры:

  >**git add --help**

  >**git branch --help**

  
