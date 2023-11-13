# Workshop-3
Идеальный баланс

Отчет по лабораторной работе #3 выполнил(а):
- Штаппер Григорий Алексеевич
- РИ-220944
  
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

Структура отчета

- Задание 1.
- Ссылка на Google Документы.
- Задание 2.
- Код реализации выполнения задания.

## Задание 1
### Предложите вариант изменения найденных переменных для 10 уровней в игре. Визуализируйте изменение уровня сложности в таблице.

https://docs.google.com/spreadsheets/d/1RZJmFMXym4TlBwado694JVUt_JqkNgFi0uHUrM8B4rw/edit#gid=0

## Задание 2
### Создать 10 сцен на Unity с изменяющимся уровнем сложности.



## Задание 3
### Заполнить таблицу данными из Python.Данные визуализировать.

https://docs.google.com/spreadsheets/d/1R1PXARr9E0pX9N3GpGgvM8DjAj0qPXC-8OFASh44Bo0/edit#gid=0
```py

import gspread
import numpy as np
gc = gspread.service_account(filename="dragonpickerdifficultylevels-3ff2d8edd3e2.json")
sh = gc.open("DragonPickerDifficultyLevels")
speed = 4
border = 5
egg_drop = 0.005
time_egg_drop = 5.5
level = list(range(1, 10))
i = 0


while i <= len(level):
    i += 1
    if i == 0: continue
    else:
        if i > 1:
            speed += 1
            if i%2 != 0: border += 1
            egg_drop += 0.0025
            time_egg_drop -= 0.5
        sh.sheet1.update(('A' + str(i+2)), i)
        sh.sheet1.update(('B' + str(i+2)), speed)
        sh.sheet1.update(('C' + str(i+2)), border)
        sh.sheet1.update(('D' + str(i+2)), egg_drop)
        sh.sheet1.update(('E' + str(i+2)), time_egg_drop)

```


## Выводы

- Была описана игровая переменная.
- С помощью скрипта на языке Python была заполнена и визуализирована таблица изменения игровой переменной.
- Была настроена сцена Unity для воспроизведения звуковых файлов. 

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
