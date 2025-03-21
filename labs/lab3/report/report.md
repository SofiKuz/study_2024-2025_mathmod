---
## Front matter
title: "Отчет по лабораторной работе №3"
subtitle: "Модель боевых действий"
author: "Кузнецова София Вадимовна"

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
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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

Построить графики модели боевых действий, а также ознакомиться с Scilab.

# Задание

**Вариант 31**  
  Задача: Между страной Х и страной У идет война. Численность состава войск 
исчисляется от начала войны, и являются временными функциями x(t) и y(t). В
начальный момент времени страна Х имеет армию численностью 33 700 человек,
а в распоряжении страны У армия численностью в 22 400 человек. Для упрощения
модели считаем, что коэффициенты a,b,c,h постоянны. 
постоянны. Также считаем P(t) и Q(t) непрерывные функции.
  Постройте графики изменения численности войск армии Х и армии У для
следующих случаев: 

1. Модель боевых действий между регулярными войсками  
  $\frac{\partial x}{\partial t} = -0,44x(t)-0,78y(t)+sin(3t) + 1$  
  $\frac{\partial y}{\partial t} = -0,56x(t)-0,66y(t)+cos(3t) + 1$

2. Модель ведение боевых действий с участием регулярных войск и
партизанских отрядов  
  $\frac{\partial x}{\partial t} = -0,37x(t)-0,79y(t)+sin(2t)+1$  
  $\frac{\partial y}{\partial t} = -0,27x(t)y(t)-0,78y(t)+cos(2t)+1$

# Выполнение лабораторной работы

**1. Рассмотрим подробнее уравнения**

1.1. Потери, не связанные с боевыми действиями, описывают члены -0,44x(t) и -0,78y(t), 
члены -0,66y(t) и -0,56x(t) отражают потери на поле боя. Функции P(t)=sin(3t)+1, Q(t)=cos(3t)+1 учитывают
возможность подхода подкрепления к войскам Х и У в течение одного дня. 

1.2. Потери, не связанные с боевыми действиями, описывают члены -0,37x(t) и -0,79y(t), 
члены -0,78y(t) и -0,27x(t)y(t) отражают потери на поле боя. Функции P(t)=sin(2t)+1, Q(t)=cos(2t)+1 учитывают
возможность подхода подкрепления к войскам Х и У в течение одного дня. 
  
1.3. Начальные условия для обоих случаев будут равно $x_{0}=33700$, $y_{0}=22400$

**2. Построение графиков численности войск**

2.1. Напишем первую программу для Scilab:
```

//начальные условия
x0 = 33700;
y0 = 23400;
t0 = 0;

a = 0.44;
b = 0.78;
c = 0.56;
h = 0.66;

tmax = 1;

dt = 0.05;

t = [t0:dt:tmax];

function p = P(t)
p = sin(3*t) + 1;
endfunction

function q = Q(t)
q = cos(3*t) + 1;
endfunction

//Система дифференциальных уравнений
function dy = syst(t, y)
dy(1) = - a*y(1) - b*y(2) + P(t);
dy(2) = - c*y(1) - h*y(2) + Q(t);
endfunction

v0 = [x0;y0];

//Решение системы
y = ode(v0,t0,t,syst);

//Построение графиков решений
scf(0);
plot2d(t,y(1,:),style=2);
xtitle('Модель боевых действий № 1','Шаг','Численность армии');
plot2d(t,y(2,:), style = 5);
xgrid();

```
В результате выполнения кода мы получаем следующий график 

![Модель боевых действий № 1](image/2.png){#fig:001 width=100%}

2.2. Напишем вторую программу для Scilab:
```
x0 = 33700;
y0 = 23400;
t0 = 0;

a = 0.17;
b = 0.65;
c = 0.31;
h = 0.28;

tmax = 1;

dt = 0.05;

t = [t0:dt:tmax];

function p = P(t)
p = sin(2*t)+1;
endfunction

function q = Q(t)
q = cos(t)+1;
endfunction

//Система дифференциальных уравнений
function dy = syst(t, y)
dy(1) = - a*y(1) - b*y(2) + P(t);
dy(2) = - c*y(1)*y(2) - h*y(2) + Q(t);
endfunction

v0 = [x0;y0];

y = ode(v0,t0,t,syst);

scf(0);
plot2d(t,y(1,:),style=2);
xtitle('Модель боевых действий № 2','Шаг','Численность армии и парт. отрядов');
plot2d(t,y(2,:), style = 5);
xgrid();

```
В результате выполнения кода мы получаем следующий график 

![Модель боевых действий № 2](image/4.png){#fig:002 width=100%}

# Выводы

В результате выполнения лабораторной работы мы научились решать и строить графики модели боевых действий в среде Scilab.
