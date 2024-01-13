Задание 1
Что нужно сделать:

Установите себе jenkins по инструкции из лекции или любым другим способом из официальной документации. Использовать Docker в этом задании нежелательно.
Установите на машину с jenkins golang.
Используя свой аккаунт на GitHub, сделайте себе форк репозитория. В этом же репозитории находится дополнительный материал для выполнения ДЗ.
Создайте в jenkins Freestyle Project, подключите получившийся репозиторий к нему и произведите запуск тестов и сборку проекта go test . и docker build ..
В качестве ответа пришлите скриншоты с настройками проекта и результатами выполнения сборки.
 
Решение 1

![ALT TEXT](https://github.com/mezhibo/sys-pattern-homework/blob/389952993b61930fa6b5728631bec66a8f512015/img/jenkins1.jpg)
![ALT TEXT](https://github.com/mezhibo/sys-pattern-homework/blob/7d8ae9daecd346bc7065eea070f25f609c98a47e/img/jenkins2.jpg)


Задание 2
Что нужно сделать:

Создайте новый проект pipeline.
Перепишите сборку из задания 1 на declarative в виде кода.
В качестве ответа пришлите скриншоты с настройками проекта и результатами выполнения сборки.

Решение 2

![ALT TEXT](https://github.com/mezhibo/sys-pattern-homework/blob/1b3e30f038e87798aeb30d962ef3989986660dd9/img/jenkins6.jpg)
![ALT TEXT](https://github.com/mezhibo/sys-pattern-homework/blob/1b3e30f038e87798aeb30d962ef3989986660dd9/img/jenkins3.jpg)
![ALT TEXT](https://github.com/mezhibo/sys-pattern-homework/blob/1b3e30f038e87798aeb30d962ef3989986660dd9/img/jenkins4.jpg)
![ALT TEXT](https://github.com/mezhibo/sys-pattern-homework/blob/1b3e30f038e87798aeb30d962ef3989986660dd9/img/jenkins5.jpg)



Задание 3
Что нужно сделать:

Установите на машину Nexus.
Создайте raw-hosted репозиторий.
Измените pipeline так, чтобы вместо Docker-образа собирался бинарный go-файл. Команду можно скопировать из Dockerfile.
Загрузите файл в репозиторий с помощью jenkins.
В качестве ответа пришлите скриншоты с настройками проекта и результатами выполнения сборки.

Решение 3

Устновим Nexus 

![ALT TEXT](https://github.com/mezhibo/sys-pattern-homework/blob/b707c01179ac9043a052a5ab0b796001688eee56/img/NEXUS1.png)

Создаем репозиторий

![ALT TEXT](https://github.com/mezhibo/sys-pattern-homework/blob/b707c01179ac9043a052a5ab0b796001688eee56/img/NEXUS2.png)

Создаем новую джобу которая будет отправлять на удаленную репу нексуса файил README.md

![ALT TEXT](https://github.com/mezhibo/sys-pattern-homework/blob/b0248ff4db6fe27998d5cf54c7fe8a3bd3e5c38e/img/jenkins7.jpg)

Запускаем пайплайн и получаем SUCCESS

![ALT TEXT](https://github.com/mezhibo/sys-pattern-homework/blob/b0248ff4db6fe27998d5cf54c7fe8a3bd3e5c38e/img/jenkins8.jpg)

Идем в нексус и смотрим что появился наш фаилик README.md

![ALT TEXT](https://github.com/mezhibo/sys-pattern-homework/blob/b0248ff4db6fe27998d5cf54c7fe8a3bd3e5c38e/img/jenkins9.jpg)


