---
## Front matter
title: "Отчёт по лабороторной работе №3"
subtitle: "Архитектура компьютера"
author: "Николенко Анна Николаевна"

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
lot: true # List of tables
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
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Цель работы заключается в освоении процедуры оформления отчетов с помощью легковесного
языка разметки Markdown.

Цель данного шаблона --- максимально упростить подготовку отчётов по
лабораторным работам.  Модифицируя данный шаблон, студенты смогут без
труда подготовить отчёт по лабораторным работам, а также познакомиться
с основными возможностями разметки Markdown.

# Задание

1. В соответствующем каталоге сделайте отчёт по лабораторной работе No 2 в формате
Markdown. В качестве отчёта необходимо предоставить отчёты в 3 форматах: pdf, docx
и md.
2. Загрузите файлы на github.

# Теоретическое введение

Здесь описываются теоретические аспекты, связанные с выполнением работы.

Например, в табл. @tbl:std-dir приведено краткое описание стандартных каталогов Unix.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |

Более подробно об Unix см. в [@gnu-doc:bash;@newham:2005:bash;@zarrelli:2017:bash;@robbins:2013:bash;@tannenbaum:arch-pc:ru;@tannenbaum:modern-os:ru].

# Выполнение лабораторной работы

Открываю терминал, перехожу в каталог arch-pc (рис. [-@fig:001]).

![Открытие терминала и переход в каталог arch-pc](image/l31.png){#fig:001 width=70%}

Обновляю локальный репозиторий, введя команду git pull (рис. [-@fig:002]).

![Обновление локального репозитория](image/l3.2.png){#fig:002 width=70%}

Перехожу в каталог с шаблоном отчёта по лабороторной работе №3 (рис. [-@fig:003]).

![Переход в директорию с шаблоном отчёта](image/l3.3.png){#fig:003 width=70%}

Провожу компиляцию шаблона с использованием Makefile, введя команду make (рис. [-@fig:004]).

![Компиляция шаблона с использованием Makefile](image/l3.4.png){#fig:004 width=70%}

Проверяю корректность полученных файлов через каталоги (рис. [-@fig:005]).

![Проверка наличия файлов в папке](image/l3.5.png){#fig:005 width=70%}

Удаляю полученные файлы с использованием Makefile ранее, ввожу для этого команду make clean (рис. [-@fig:006]).

![Удаление файлов](image/l3.6.png){#fig:006 width=70%}

Проверяю, что после этой команды файлы report.pdf и report.docx были удалены (рис. [-@fig:007]).

![Проверка отсутствия файлов](image/l3.7.png){#fig:007 width=70%}

Открываем файл report.md c помощью текстового редактора gedit (рис. [-@fig:008]).

![Открытие файла report.md](image/l3.8.png){#fig:008 width=70%}

Заполнила отчет и скомпилировала его с использованием Makefile. Проверила корректность полученных файлов. Загрузила файлы на Github.







# Выводы

Здесь кратко описываются итоги проделанной работы.

# Список литературы{.unnumbered}

::: {#refs}
:::
