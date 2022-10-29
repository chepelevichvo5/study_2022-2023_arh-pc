---
## Front matter
title: "Отчёт по лабораторной работе № 3"
subtitle: "НКАбд-04-22"
author: "Чепелевич Владислав Олегович"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Целью работы является изучить идеологию и применение средств 
контроля версий. Приобрести практические навыки по работе с системой git.

# Задание

1. Настроить github
2. Выполнить базовую настройку git
3. Создать SSH ключа
4. Создать рабочее пространство на основе шаблона
5. Создать репозиторий курса на основе шаблона
6. Настроить каталог курса
7. Выполнить задание для самостоятельной работы

# Выполнение лабораторной работы

## Настройка github

Создали учётную запись на сайте https://github.com/ и заполнили 
основные данные. (рис. [-@fig:001])
![Заполнили основные данные](image/1.jpg){ #fig:001 width=70% }
![Создание профиля на сайте https://github.com/](image/2.jpg){ #fig:002 width=70% }

## Базовая настройка git

Сначала сделали предварительную конфигурацию git. Открыли 
терминал и ввели следующие команды, указав имя и email владельца 
репозитория. (рис. [-@fig:003])

![Создание предварительной конфигурации git](image/3.jpg){ #fig:003 width=70% }

Настроили utf-8 в выводе сообщений git. (рис. [-@fig:004])

![Настройка utf-8 в выводе сообщений git](image/4.jpg){ #fig:004 width=70% }

Задали имя начальной ветки (назвали её master). (рис. [-@fig:005])

![master](image/5.jpg){ #fig:005 width=70% }

Параметр autocrlf. (рис. [-@fig:006])

![autocrlf](image/6.jpg){ #fig:006 width=70% }

Параметр safecrlf. (рис. [-@fig:007])

![safecrlf](image/7.jpg){ #fig:007 width=70% }

## Создание SSH ключа

Для последующей идентификации пользователя на сервере 
репозиториев сгенерировали пару ключей (приватный и открытый). (рис. [-@fig:008])

![Генерация ключей](image/8.jpg){ #fig:008 width=70% }

![Генерация ключей](image/9.jpg){ #fig:009 width=70% }
Для загрузки сгенерённого открытого ключа зашли на сайт 
http://github.org/ под своей учётной записью и перешли в меню Setting . После 
этого выбрали в боковом меню SSH and GPG keys и нажали кнопку New SSH 
key . Скопировав из локальной консоли ключ в буфер обмена, вставили его в 
появившееся на сайте поле и указали для ключа имя (Title). (рис. [-@fig:009]),
(рис. [-@fig:010]), (рис. [-@fig:011])

![Копирование ключа](image/10.jpg){ #fig:010 width=70% }

![Загрузка ключа на GitHub (1)](image/11.jpg){ #fig:011 width=70% }

![Загрузка ключа на GitHub (2)](image/12.jpg){ #fig:012 width=70% }

##  Сознание рабочего пространства и репозитория курса на основе шаблона

Открыли терминал и создали каталог для предмета «Архитектура 
компьютера». (рис. [-@fig:013])

![Создание каталога “Архитектура компьютера”](image/13.jpg){ #fig:013 width=70% }

## Сознание репозитория курса на основе шаблона

Перешли на станицу репозитория с шаблоном курса, 
https://github.com/yam adharma/course-directory-student-template, и выбрали 
Use this template. (рис. [-@fig:014])

![Выбор шаблона](image/14.jpg){ #fig:014 width=70% }

Открыли терминал и перешли в каталог курса. (рис. [-@fig:015])

![Переход в каталог курса](image/15.jpg){ #fig:015 width=70% }

Клонировали созданный репозиторий. Ссылку для клонирования 
скопировали на странице созданного репозитория Code -> SSH. (рис. [-@fig:016])

![Копирование ссылки для клонирования](image/16.jpg){ #fig:016 width=70% }

![Клонирование репозитория](image/17.jpg){ #fig:017 width=70% }

## Настройка каталога курса

Перешли в каталог курса. (рис. [-@fig:018]) Удалили лишние файлы. (рис. [-@fig:019])
Создали необходимые каталоги. (рис. [-@fig:020]) Отправили файлы на сервер 
(рис. [-@fig:021])Проверили правильность создания иерархии рабочего пространства в локальном репозитории и на странице github. (рис. [-@fig:022]), (рис. [-@fig:023])

![Каталог курса](image/18.jpg){ #fig:018 width=70% }

![Удаление лишних файлов](image/19.jpg){ #fig:019 width=70% }

![ Создание каталогов](image/20.jpg){ #fig:020 width=70% }

![Отправление файлов на сервер ](image/21.jpg){ #fig:021 width=70% }

![Проверка правильности создания иерархии рабочего пространства на странице github](image/22.jpg){ #fig:022 width=70% }

![Проверика правильности создания иерархии рабочего пространства в локальном репозитории](image/23.jpg){ #fig:023 width=70% }

## Задание для самостоятельной работы

1. Создали отчет по выполнению лабораторной работы в 
соответствующем каталоге рабочего пространства (labs>lab03>report)
Скопировали отчеты по выполнению предыдущих лабораторных работ 
в соответствующие каталоги созданного рабочего пространства. (рис. [-@fig:026]),
(рис. [-@fig:027])

![Скопированный отчет 2](image/26.jpg){ #fig:026 width=70% }

![Скопированный отчет 1](image/27.jpg){ #fig:027 width=70% }

Загрузили файлы на github. (рис. [-@fig:024]), (рис. [-@fig:025]),
(рис. [-@fig:028])

![Загруженный отчет 1](image/24.jpg){ #fig:024 width=70% }

![Загруженный отчет 2](image/25.jpg){ #fig:025 width=70% }

![Загруженный отчет 3](image/28.jpg){ #fig:028 width=70% }


# Выводы
В ходе работы были изучены идеология и применение средств 
контроля версий. Были приобретены практические навыки по работе с 
системой git. 


