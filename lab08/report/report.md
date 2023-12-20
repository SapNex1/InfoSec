---
# Front matter
title: "Лабораторная работа №8. Целочисленная арифметика многократной точности."
subtitle: "Предмет: Математические основы защиты информации и информационной безопасности"
author: "Александр Сергеевич Баклашов"

# Generic otions
lang: ru-RU
toc-title: "Содержание"

# Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

# References settings
linkReferences: true
nameInLink: true

# Pdf output format
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: false # List of tables
fontsize: 12pt
linestretch: 1.25
papersize: a4
documentclass: scrreprt
## I18n
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
### Fonts
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
## Misc options
indent: true
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Рассмотреть и реализовать алгоритмы для выполнения арифметических операций с большими целыми числами.

# Задание

Реализовать алгоритмы для выполнения арифметических операций с большими целыми числами.

# Теоретическое введение

Данные алгоритмы позволяют складывать, вычитать, умножать и делить числа различных систем счисления. 

# Выполнение лабораторной работы

## Алгоритм 1 (сложение неотр. целых чисел)

### Задача

Реализовать алгоритм для сложения неотрицательных целых чисел.

#### Решение

Реализуем алгоритм для сложения неотрицательных целых чисел  (рис. [-@fig:001])

![Алгоритм 1](image/1.png){ #fig:001 width=80% }

## Алгоритм 2 (вычитание неотр. целых чисел)

### Задача

Реализовать алгоритм для вычитания неотрицательных целых чисел.

#### Решение

Реализуем алгоритм для вычитания неотрицательных целых чисел  (рис. [-@fig:002])

![Алгоритм 2](image/2.png){ #fig:002 width=80% }

## Алгоритм 3 (умножение неотр. целых чисел столбиком)

### Задача

Реализовать алгоритм для умножения целых чисел столбиком.

#### Решение

Реализуем алгоритм для умножения целых чисел столбиком  (рис. [-@fig:003])

![Алгоритм 3](image/3.png){ #fig:003 width=80% }

## Алгоритм 4 (быстрый столбик)

### Задача

Реализовать алгоритм для умножения целых чисел быстрым столбиком.

#### Решение

Реализуем алгоритм для умножения целых чисел быстрым столбиком (рис. [-@fig:004])

![Алгоритм 4](image/4.png){ #fig:004 width=80% }

## Алгоритм 5 (деление многоразрядных целых чисел)

### Задача

Реализовать алгоритм для деления многоразрядных целых чисел

#### Решение

Реализуем алгоритм для деления многоразрядных целых чисел (рис. [-@fig:005])

![Алгоритм 5](image/5.png){ #fig:005 width=80% }

# Выводы

В ходе данной лабораторной работы я рассмотрел и реализовал алгоритмы для выполнения арифметических операций с большими целыми числами.

# Библиография

1. Python documentation. [Электронный ресурс]. М. URL: [Python documentation](https://docs.python.org/3/index.html) (Дата обращения: 28.09.2023).

2. Лабораторная работа №8. Целочисленная арифметика многократной точности. - 3 с. [Электронный ресурс]. М. URL: [Лабораторная работа №8. Целочисленная арифметика многократной точности.](https://esystem.rudn.ru/pluginfile.php/2089832/mod_folder/content/0/lab08.pdf) (Дата обращения: 20.12.2023).