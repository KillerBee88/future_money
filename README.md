# Скрипт для сбора статистики вакансий программистов на сайтах HeadHunter и SuperJob.

Основной скрипт выводит информацию в таблице о средней зарплате и количестве вакансий для программистов.

## Как установить

Python3 должен быть установлен. 
Затем используйте `pip` (или `pip3`, есть конфликт с Python2) для установки зависимостей:
```
pip install -r requirements.txt
```
Далее нужно создать файл `.env` прописать свой токен (`SUPERJOB_API_KEY`) для сайта superjob.ru. Токен можно получить по ссылке:[инструкции](https://api.superjob.ru/) 

Пример сожержимого файла .env:

```
SUPERJOB_API_KEY=ваш_токен
```

Замените ваш_токен на ваш реальный токен, который можно получить по ссылке [инструкции](https://api.superjob.ru/).

После создания файла .env скрипт будет автоматически использовать значения переменных окружения при запуске.

## Использование скриптов

Проект включает в себя несколько скриптов

### Основной скрипт `main.py`
Выводит информацию в табличной форме о средней зарплате и количестве вакансий языков программирования, для двух площадок HeadHunter и SuperJob.

Пример запуска:
```
python main.py
```
На выходе в консоль выведет две таблицы:

![Пример](https://i.ibb.co/m953dxT/Screenshot-1.png)

### Скрипт `hh_vacancies.py`
Выводит информацию в табличной форме о средней зарплате и количестве вакансий языков программирования на HeadHunter (г.Москва).

Принимает обязательный аргумент: 
* "-l", "--languages", - список языков программирования для поиска вакансий.


Пример запуска:
```
python hh_vacancies.py -l 'Python', 'C++', 'Java'
```
Пример работы аналогичен основному скрипту.

### Скрипт `sj_vacancies.py`
Выводит информацию в таблице о средней зарплате и количестве вакансий языков программирования на SuperJob (г.Москва).

Принимает обязательный аргумент: 
* "-l", "--languages", - список языков программирования для поиска вакансий.


Пример запуска:
```
python sj_vacancies.py -l 'Python', 'C++', 'Java'
```
Пример работы аналогичен основному скрипту.
