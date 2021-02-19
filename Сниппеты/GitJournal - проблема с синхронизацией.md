# GitJournal - проблема с синхронизацией

Наткнулся на проблемы в [GitJournal](https://gitjournal.io/):

- Бесконечное клонирование репозитория  https://github.com/GitJournal/GitJournal/issues/417
- Не пуллились изменения с сервера на андроид https://github.com/GitJournal/GitJournal/issues/361

В логах была ошибка `Got Exception Exception: Current Branch null #0 ...`.

Покурив/покумекав решил скопипастить конфиг гита с ноута из файла `.git/config`, а именно строчки

```ini
[branch "master"]
	remote = origin
	merge = refs/heads/master
```

в `.git/config` на Андроиде.

Потом сделал тестовые изменения и запушил с Андроида и вроде после этого проблем не было.
