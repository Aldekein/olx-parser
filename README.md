## ОЛХ парсер
### Возможности
##### Скачивание данных с объявлений ОЛХ по поисковому запросу
##### Сохранение данных в csv формате
##### RSS лента для отслеживаия поискового запроса

#### Установка
```bash
git clone https://github.com/lerdem/olx-parser
cd olx-parser/
# set urls for serarch/monitor in configuration.json
docker-compose up -d --build
# run for creating empty .csv files
docker exec -it olx-server python -m ad.adapters.repository
```
После выполненых шагов установки, подключите rss ссылку http://<ip где установлен server>:12345/detail-rss в свой rss ридер


#### Планы
- [ ] Вестка шаблона html для rss ридера
- [ ] Семантическое версионирование
- [ ] Упростить хранение csv(хранить частями со сборкой в конце)
- [ ] Парсинг номеров телефонов
- [ ] Причины написания парсера
- [ ] Конфигурация поиска объявлений (из url/form)
- [ ] Возможность добавления нескольких запросов на мониторинг
- [ ] Добавить скрипт по генерации changelog на базе коммитов
- [ ] Добавить альтернативу RSS
- [ ] ad/adapters/presenter.py:23 url из config файла
