## __Лабораторная работа №6__
### __Система контроля версий__
_Цель лабораторной работы_: изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.
# Ход выполнения лабораторной работы
> Скриншоты лабораторной работы находятся в папке screenshots, каждый из них имеет название, соответствующее номеру пункта, выполнение которого необходимо подкрепить этим самым скриншотом. Например, скриншот для пункта 1 соответственно имеет название _1.PNG_
## Пункт 1
Необходимо создать аккаунт на сайте GitHub (_см. [рис. 1](https://github.com/ArsenValeev/LR6/blob/report/screen/png1.png)_). 
## Пункт 2
Далее при помощи Fork создается копия [репозитория лабораторной работы](https://github.com/Kurtyanik/LR6/) в личное хранилище (_см. [рис. 2](https://github.com/ArsenValeev/LR6/blob/report/screen/png2.png)_).
## Пункт 3
Соглано лабораторной работе, необходимо установить Git (_см. [рис. 3](https://github.com/ArsenValeev/LR6/blob/report/screen/png3.png)_).
## Пункт 4
Далее с помощью _git config --global user_name_ и _git config --global user_email_ был настроен клиент git (_см. [рис. 4](https://github.com/ArsenValeev/LR6/blob/report/screen/png4.png)_).
## Пункт 5
Затем на диске С в папке lab6op была создана копия своего личного удалённого репозитория на компьютер (_см. [рис. 5](https://github.com/ArsenValeev/LR6/blob/report/screen/png5.png)_).
## Пункт 6
Теперь нужно добавить файл через интерфейс GitHub и подтянуть изменения в локальный репозиторий. На скриншоте 6 (_см. [рис. 6](https://github.com/ArsenValeev/LR6/blob/report/screen/png6.png)_) представлены файлы, находящиеся в локальном репозитории, до обновленния данных и после. Их поиск осуществляется командой _ls -1_, а обновление информации - _git pull_.
## Пункты 7, 8
Далее необходимо получить историю операций для веток и просмотреть последние изменения. Первое осуществлялось с помощью команды _git reflog branch_name_, а второе - с помощью _log_ (_см. [рис. 7, 8](https://github.com/ArsenValeev/LR6/blob/report/screen/png7-8.png)_).
## Пункт 9
Затем нужно выполнить слияние в ветку master. С помощью команды _git merge branch_name_ ветки _master_ и _other_master_ были объединены (содержимое other_master появилось в ветке master, _см. [рис. 9](https://github.com/ArsenValeev/LR6/blob/report/screen/png9.png)_).
## Пункт 10
Теперь необходимо удалить побочную ветку. Для этого была использована команда _git branch -d branch_name_ (_см. [рис. 10](https://github.com/ArsenValeev/LR6/blob/report/screen/png10.png)_).
## Пункт 11
Для наглядной работы с репозиторием необходимо сделать изменения и зафиксировать их, оставляя комментарии. Поочередно в репозиторий были добавлены три текстовых файла: task1.txt, task2.txt, task3.txt, созданные командой _echo "text" >> name.txt_. Изменения фиксировались командой _git add_, для создания коммита - _git commit -m "text"_, для обновления информации в репозитории - _git push_ (_см. [рис. 11.1](https://github.com/ArsenValeev/LR6/blob/report/screen/png11.1.png); [рис. 11.2](https://github.com/ArsenValeev/LR6/blob/report/screen/png11.2.png); [рис. 11.3](https://github.com/ArsenValeev/LR6/blob/report/screen/png11.3.png)_).
## Пункт 12
С помощью _git revert HEAD --no-edit_ был осуществлен откат коммита (_см. [рис. 12](https://github.com/ArsenValeev/LR6/blob/report/screen/png12.png)_).

# Лог команд
git config --global user.name "Arsen Valeev

git config --global user.email "arsenvaleev123@gmail.com "

mkdir lab6op

cd / c/ lab6op 

git clone https://github.com/dmit-p0/LR6

git pull

ls -1

git reflog

git log
	
git branch other_master
git checkout other_master

ls -1

git checkout master

ls -1

git merge other_master

ls -1

git branch -d other_master

echo "Первый файл" >> task1.txt

git status

git add task1.txt

git status

git commit -m "Первый commit"

git push

echo "Второй файл" >> task2.txt

git status

git add task2.txt

git status

git commit -m "Второй commit"

git push

echo "Третий файл" >> task3.txt

git status

git add task3.txt

git status

git commit -m "Третий commit"

git push

git revert HEAD --no-edit

# История операций
С помощью команды _git log --pretty=format:"%h - %ad - %an: %s" --date=short_ была получена история операций в укороченном виде.

bcface9 - 2024-11-14 - Arsen Valeev: Revert "Третий commit"

64f9f22 - 2024-11-14 - Arsen Valeev: Третий commit

d9bb47d - 2024-11-14 - Arsen Valeev: Второй commit

271d37e - 2024-11-14 - Arsen Valeev: Первый commit

1a3a11e - 2024-11-14 - Arsen Valeev: other

b291c26 - 2024-11-14 - ArsenValeev: Create new_file

921f53b - 2020-11-21 - Kurtyanik: Обновление информации

c08a654 - 2020-11-21 - Kurtyanik: Файл создан пустым

3c6e913 - 2020-11-21 - Kurtyanik: Initial commit

