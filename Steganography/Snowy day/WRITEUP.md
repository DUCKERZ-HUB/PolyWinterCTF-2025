# Снежный день | easy | steganography

## Информация
> Очень люблю снег! Снеговики, снежные замки, снежки! СНЕГ! СНЕГ! СНЕГ!

## Выдать участникам
файл [snowy_day.zip](public/snowy_day.zip)

## Описание
Для решения необходимо использовать утилиту `stegsnow` без кодового слова

## Решение
Дается текстовый файл. Если в нем выделить все символы, то можно увидеть, что внутри файла много лишних табуляций и пробелов. 

Учитывая название таска и его описание, то можно прийти к выводу, что информация спрятана с помощью утилиты `stegsnow`. 

Для того, чтобы получить спрятанную информацию, достаточно использовать следующую команду:

`stegsnow -C task.txt`

## Флаг
`PolyCTF{m0r3_sp4c3s_f0r_sn0w}`
