---
## Front matter
lang: ru-RU
title: Лабораторная работы №1
subtitle: Git
author:
  - Кузнецова С. В.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 20 февраля 2025

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Кузнецова София Вадимовна
  * Российский университет дружбы народов

:::
::: {.column width="30%"}

:::
::::::::::::::


# Ход работы

## Подготовка

![Имя и электронная почта](image/1.png){ #fig:001 width=65% }

![Сore.autocrlf с параметрами true и input](image/2.png){ #fig:002 width=65% }
    	   	
![Флаг](image/3.png){ #fig:003 width=65% }

## Создание проекта

![Создание файла hello.html](image/4.png){ #fig:004 width=80% }

## Внесение изменений

![Изменение файла hello.html](image/5.png){ #fig:005 width=60% }

![Состояние каталога](image/6.png){ #fig:006 width=60% }

## Коммит изменений

![Git commit](image/7.png){ #fig:007 width=40% }
	
![Комментарий: «Added h1 tag»](image/8.png){ #fig:008 width=40% }

![Состояние каталога](image/9.png){ #fig:09 width=40% }

## Добавление тегов

![Добавим стандартные теги <html> и <body>](image/10.png){ #fig:010 width=40% }

![Добавление изменения](image/11.png){ #fig:011 width=40% }

![Добавим секцию <head>](image/12.png){ #fig:012 width=40% }

## Коммит

![Коммит](image/13.png){ #fig:013 width=55% }

## История

![Список произведенных изменений](image/14.png){ #fig:014 width=30% }

![Однострочный формат истории. Много вариантов отображения лога. Справочная страница.](image/15.png){ #fig:015 width=30% }

## Получение старых версий

![Хэши предыдущих версий](image/16.png){ #fig:016 width=30% }

![Хэш-код](image/17.png){ #fig:017 width=30% }

## Cоздание тегов версий. Переключение по имени тега

![Теги](image/18.png){ #fig:018 width=30% }

![Перекоючение между двумя отмеченными версиями](image/19.png){ #fig:019 width=30% }

## Просмотр тегов с помощью команды tag

![Теги в логе](image/20.png){ #fig:020 width=80% }

## Отмена локальных изменений (до индексации)

![Коммите ветки master](image/21.png){ #fig:021 width=20% }

![Нежелательный комментарий](image/22.png){ #fig:022 width=20% }

![Состояние каталога](image/23.png){ #fig:023 width=20% }

![Команда git checkout](image/24.png){ #fig:024 width=20% }

## Отмена проиндексированных изменений (перед коммитом)

![Нежелательный комментарий](image/25.png){ #fig:025 width=50% }

![Нежелательный комментарий](image/26.png){ #fig:026 width=50% }

## Отмена проиндексированных изменений (перед коммитом)

![Состояние нежелательного изменения](image/27.png){ #fig:027 width=40% }

![Отмена индексации изменения](image/28.png){ #fig:028 width=40% }

![Версия коммита](image/29.png){ #fig:029 width=40% }

## Отмена коммитов

![Изменение файла hello.html](image/30.png){ #fig:030 width=50% }

![Выполнение команд](image/31.png){ #fig:031 width=50% }

## Отмена коммитов

![Отмена коммита](image/32.png){ #fig:032 width=30% }

![Проверка лога](image/33.png){ #fig:033 width=30% }

## Удаление коммиттов из ветки

![История коммитов](image/34.png){ #fig:034 width=50% }

![Отметка последнего коммита тегом](image/35.png){ #fig:035 width=50% }

## Удаление коммиттов из ветки

![Сброс ветки](image/36.png){ #fig:036 width=25% }

![Просмотр коммитов](image/37.png){ #fig:037 width=20% }

## Удаление тега oops

![Тег oops](image/38.png){ #fig:038 width=50% }

## Внесение изменений в коммиты

![Комментарий автора](image/39.png){ #fig:039 width=50% }

![Коммит](image/40.png){ #fig:040 width=50% }

## Внесение изменений в коммиты

![Комментарий email ](image/41.png){ #fig:041 width=30% }

![Изменения предыдущего коммита](image/42.png){ #fig:042 width=35% }

![История коммитов](image/43.png){ #fig:043 width=20% }

## Перемещение файлов. Второй способ перемещения файлов

![Каталог lib](image/44.png){ #fig:044 width=40% }

![Идентичный набор команд](image/45.png){ #fig:045 width=40% }

![Коммит перемещения](image/46.png){ #fig:046 width=40% }

## Подробнее о структуре

![Добавление файла index.html](image/47.png){ #fig:047 width=60% }

![Добавление файла и создание коммита](image/48.png){ #fig:048 width=60% }

## Git внутри: Каталог .git

![Просмотр каталога в котором хранится вся информация git](image/49.png){ #fig:049 width=80% }

## Работа непосредственно с объектами git

![Просмотр последнего коммита](image/50.png){ #fig:050 width=50% }

## Создание ветки. Добавление файлы стилей style.css. Создание файла. 

![Ветка «style»](image/51.png){ #fig:051 width=30% }

![Файл стилей style.css](image/52.png){ #fig:052 width=30% }

![Редактируем файл](image/53.png){ #fig:053 width=30% }

![Коммит](image/54.png){ #fig:054 width=30% }

## Обновление файла hello.html

![Обновление файла hello.html](image/55.png){ #fig:055 width=25% }

![Коммит](image/56.png){ #fig:056 width=25% }

![Обновление файла index.html](image/57.png){ #fig:057 width=25% }

![Коммит](image/58.png){ #fig:058 width=25% }

## Навигация по веткам

![Просмотр проекта](image/59.png){ #fig:059 width=15% }

![Команда git checkout](image/60.png){ #fig:060 width=15% }

![Ветка style](image/61.png){ #fig:061 width=15% }

## Изменения в ветке master

![Файл README](image/62.png){ #fig:062 width=100% }

## Создаётся коммит изменений README.md в ветку master.

![Коммит изменений README.md](image/63.png){ #fig:063 width=50% }

## Слияние

![Солияние master с style](image/64.png){ #fig:064 width=40% }

## Создание конфликта

![Ветку master](image/65.png){ #fig:065 width=50% }

![Изменения в ветке master](image/66.png){ #fig:066 width=50% }

## Создание конфликта

![Коммит](image/67.png){ #fig:067 width=40% }

![Просмотр веток](image/68.png){ #fig:068 width=35% }

## Разрешение конфликтов

![Слияние master с веткой style](image/69.png){ #fig:069 width=25% }

![Файл lib/hello.html](image/70.png){ #fig:070 width=20% }

![Разрешение конфликта](image/71.png){ #fig:071 width=25% }

![Коммит](image/72.png){ #fig:072 width=25% }

## Сброс ветки style

![Коммит перед слиянием](image/73.png){ #fig:073 width=10% }

![Updated index.html](image/74.png){ #fig:074 width=30% }

![Лог ветки style](image/75.png){ #fig:075 width=15% }

## Сброс ветки master

![Интерактивный режим в ветке master](image/76.png){ #fig:076 width=25% }

![Коммит «Added README»](image/77.png){ #fig:077 width=25% }

## Перебазирование

![Команда git rebase](image/78.png){ #fig:078 width=55% }

## Слияние в ветку master

![Style в master](image/79.png){ #fig:079 width=45% }

## Клонирование репозиториев

![Клон репозитория hello](image/80.png){ #fig:080 width=85% }

## Просмотр клонированного репозитория

![Клон](image/81.png){ #fig:081 width=60% }

## Origin

![Оrigin](image/82.png){ #fig:082 width=85% }

## Удаленные ветки

![Удалённые ветки](image/83.png){ #fig:083 width=90% }

## Изменение оригинального репозитория

![Репозиторий hello](image/84.png){ #fig:084 width=40% }

![Файл README.md](image/85.png){ #fig:085 width=40% }

![Коммит](image/86.png){ #fig:086 width=40% }

## Изменение оригинального репозитория

![Извлечение изменений](image/87.png){ #fig:087 width=35% }

![Проверка README.md](image/88.png){ #fig:088 width=35% }

## Слияние извлеченных изменений

![Файл README.md](image/89.png){ #fig:089 width=40% }

![Локальная ветка](image/90.png){ #fig:090 width=40% }

## Добавление ветки наблюдения

![Чистый репозиторий](image/91.png){ #fig:091 width=100% }

## Создайте чистый репозиторий

![Репозиторий hello.git](image/92.png){ #fig:092 width=100% }

## Добавление удаленного репозитория

![Файл README.md](image/93.png){ #fig:093 width=50% }

![Коммит](image/94.png){ #fig:094 width=50% }

## Извлечение общих изменений

![Клонированный репозиторий](image/95.png){ #fig:095 width=95% }

# Выводы

В ходе выполнения лабораторной работы научилась работать с git.

## {.standout}

Спасибо за внимание!
