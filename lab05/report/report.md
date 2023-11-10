---
# Front matter
title: "Лабораторная работа №5. Вероятностные алгоритмы проверки чисел на простоту."
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

Рассмотреть и реализовать алгоритмы проверки чисел на простоту.

# Задание

Реализовать следующие алгоритмы:

- Тест Ферма;

- Нахождение символа Якоби;

- Тест Соловэя-Штрассена;

- Тест Миллера-Рабина.

# Теоретическое введение

Тест Ферма:

Теория: Основан на малой теореме Ферма, которая утверждает, что если p - простое число, то для любого целого a, не кратного p, справедливо 
$a^{p-1} \equiv 1(mod \;p)$. Если обратное также верно, то p - простое. Тест Ферма использует эту теорему, проверяя условие для случайно выбранных a.

Нахождение символа Якоби:

Теория: Символ Якоби обобщает символ Лежандра и предоставляет метод определения квадратичной вычетности для нечетных простых чисел. Символ Якоби для числа a и простого нечетного числа p определяется как произведение символов Лежандра для простых множителей a по модулю p. Используется для проверки квадратичной вычетности.

Тест Соловэя-Штрассена:

Теория: Основан на том, что простые числа обладают свойством квадратичной вычетности. Если n - простое, то для любого целого числа 
a существует квадратный корень по модулю n. Тест Соловэя-Штрассена проверяет это свойство для случайно выбранных a, используя символ Якоби.

Тест Миллера-Рабина:

Теория: Основан на том, что большинство составных чисел обладают свойством "псевдопростоты" по отношению к определенному базису. Тест Миллера-Рабина проверяет это свойство для случайно выбранных базисов. Если число n не проходит тест, то оно с большой вероятностью составное.

Эти тесты предоставляют методы проверки простоты чисел, но важно отметить, что они не гарантируют абсолютную простоту и могут давать ошибочные результаты. В практике их часто комбинируют или применяют с дополнительными проверками для повышения надежности.

# Выполнение лабораторной работы

## Тест Ферма

### Задача

Реализовать тест Ферма

#### Решение

Реализуем тест Ферма  (рис. [-@fig:001])

![Тест Ферма](image/1.png){ #fig:001 width=80% }

## Нахождение символа Якоби

### Задача

Реализовать алгоритм нахождения символа Якоби

#### Решение

Найдём символ Якоби (рис. [-@fig:002])

![Символ Якоби](image/2.png){ #fig:002 width=80% }

## Тест Соловэя-Штрассена

### Задача

Реализовать тест Соловэя-Штрассена

### Решение

Реализуем тест Соловэя-Штрассена (рис. [-@fig:003])

![Тест Соловэя-Штрассена](image/3.png){ #fig:003 width=80% }

## Тест Соловэя-Штрассена

### Задача

Реализовать тест Соловэя-Штрассена

### Решение

Реализуем тест Соловэя-Штрассена (рис. [-@fig:004])

![Тест Соловэя-Штрассена](image/4.png){ #fig:004 width=80% }

# Выводы

В ходе данной лабораторной работы я рассмотрел и реализовал следующие алгоритмы:

- Тест Ферма;

- Нахождение символа Якоби;

- Тест Соловэя-Штрассена;

- Тест Миллера-Рабина.

# Библиография

1. Python documentation. [Электронный ресурс]. М. URL: [Python documentation](https://docs.python.org/3/index.html) (Дата обращения: 28.09.2023).

2. Лабораторная работа №5. Вероятностные алгоритмы проверки чисел на простоту. - 5 с. [Электронный ресурс]. М. URL: [Лабораторная работа №5. Вероятностные алгоритмы проверки чисел на простоту.](https://esystem.rudn.ru/pluginfile.php/2089811/mod_folder/content/0/lab05.pdf) (Дата обращения: 10.11.2023).