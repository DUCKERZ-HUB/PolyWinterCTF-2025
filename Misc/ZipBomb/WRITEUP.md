# ZipBomb | easy | Misc

## Информация
> Как-то долго грузится мой сайт.. Может с интернетом проблема? Да не, вроде работает..

## Выдать участникам
Ссылка [link](http://tasks.polyctf.ru:30001/)

## Описание
Для решения надо скачать сайт и разархвировать.

## Решение
При попытке загрузить сайт, у вас, скорее всего, ничего не получится. Происходит это потому, что сайт весит 10 гигабайт. Точнее, передаётся с сервера 10 мегабайт, но так как указано, что сайт сжат, то браузер пытается распаковать его, в следствие чего потребляет 10 гигабайт оперативной памяти.

Для решения проблемы нужно скачать файл таким образом, чтобы не началась распаковка. Отличным решением будет использовать команду `curl`. Но поскольку нам всё равно нужно распаковать данные, можно попробовать запустить дополнительную параллельную операцию `gzip -d`, ведь именно gzip используется для сайтов:

`curl http://tasks.polyctf.ru:30001 | gzip -d`

Так как файл имеет высокую степень сжатия, надо подождать примерно минуту, и на выходе мы получим флаг.

## Флаг
`PolyCTF{z1p_b0mb_15_funny}`
