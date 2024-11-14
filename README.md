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
Далее необходимо получить историю операций для веток и просмотреть последние изменения. Первое осуществлялось с помощью команды _git reflog branch_name_, а второе - с помощью _log_ (_см. [рис. 7, 8](https://github.com/ArsenValeev/LR6/blob/report/screen/png7_8.png)_).
## Пункт 9
Затем нужно выполнить слияние в ветку master. С помощью команды _git merge branch_name_ ветки _master_ и _other_master_ были объединены (содержимое other_master появилось в ветке master, _см. [рис. 9](https://github.com/ArsenValeev/LR6/blob/report/screen/png9.png)_).
## Пункт 10
Теперь необходимо удалить побочную ветку. Для этого была использована команда _git branch -d branch_name_ (_см. [рис. 10](https://github.com/ArsenValeev/LR6/blob/report/screen/png10.png)_).
## Пункт 11
Для наглядной работы с репозиторием необходимо сделать изменения и зафиксировать их, оставляя комментарии. Поочередно в репозиторий были добавлены три текстовых файла: task1.txt, task2.txt, task3.txt, созданные командой _echo "text" >> name.txt_. Изменения фиксировались командой _git add_, для создания коммита - _git commit -m "text"_, для обновления информации в репозитории - _git push_ (_см. [рис. 11.1](https://github.com/ArsenValeev/LR6/blob/report/screen/png11_1.png); [рис. 11.2](https://github.com/ArsenValeev/LR6/blob/report/screen/png11_2.png); [рис. 11.3](https://github.com/ArsenValeev/LR6/blob/report/screen/png11_3.png)_).
## Пункт 12
С помощью _git revert HEAD --no-edit_ был осуществлен откат коммита (_см. [рис. 12](https://github.com/ArsenValeev/LR6/blob/report/screen/png12.png)_).
