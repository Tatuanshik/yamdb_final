[![CI и CD проекта api_yamdb](https://github.com/Tatuanshik/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg?branch=master)](https://github.com/Tatuanshik/yamdb_final/actions/workflows/yamdb_workflow.yml/)


# CI и CD проекта api_yamdb
## Проект api_yamdb собирает отзывы пользователей на различные произведения. В приложении есть категории, жанры, исполнители - для удобного поиска нужного вам исполнителя. Вы можете добавить отзыв к произведению только один раз, а также комментарий к этому отзыву.
### Авторы приложение api_yamdb: Толстопятов Владимир, Яппаров Рустам, Марковская Татьяна
# Описание команд запуска приложения в контейнере и заполнения базы данными:
## Перейти в каталог для запуска контейнера
```cd yamdb_final```
```cd infra```
## Запуск docker-compose:
```docker-compose up -d --build```
## Выполнить миграции: 
```docker-compose exec web python manage.py migrate```
## Создать суперпользователя:
```docker-compose exec web python manage.py createsuperuser```
## Заполнить базу данными:
### Зайти на на сайт http://localhost/admin/
### Авторизоваться в качестве суперпользователя и добавить необходимые данные
### Выполнить миграции
### При необходимости, создать резервную копию базы данных:
```docker-compose exec web python manage.py dumpdata > fixtures.json ```

## Секретную информацию (user, host, ssh-key, etc.) добавляют в разделе настройки (Settings) в репозитарии.
## Необходимые действия:
### перейти в Settings
### слева нажать на поле Secrets --> Actions
### справа нажать на зеленую кнопку New repository secret

## Используемые технологии:
### CI/CD
### Docker/DockerHub
### docker-compose
### NGINX
### YandexCloud
### GitHub/GitActions
