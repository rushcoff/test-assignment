# Тестовое задание

## Необходимые пакеты (указаные версии используются в нашем проекте):

- typescript v3
- react v16
- react-router v4
- mobx v4
- mobx-react v5

## Задание

Написать SPA приложение, состоящее из 3-х основных компонентов:

### Страница авторизации

- При успешном вводе логина/пароля (логин пароль захардкожен – root / admin), запись в LocalStorage флага о допуске к сайту(любой ключ)
- При не успешном вводе, сообщение об ошибке – в любом, понятном для пользователя виде

### Страница с таблицей (Все поля из прикрепленного JSON’a)

- Страница 2) и страница 3) должны содержать общий header, в котором указан логин и кнопка выйти
- Первый столбец – в этом столбце значения должны быть ссылками(id = caseUid), а не текстом.
- При клике на ссылку переход на 3) компонент с передачей этого id
- К таблице должен применятся простой фильтр типа `<input />`, который фильтрует данные по всем столбцам и оставляет только те записи, которые подходят под его действие. Можно добавить дебаунсинг, но не обязательно.

### Страница с материалом

- На вход дается id
- По id получить запись из JSON’a
- Вывести эту запись на страницу в виде таблицы ключ-значение
- Страница должна содержать кнопку «Назад к таблице»
- Без авторизации(то есть без записи в localStorage) делать редирект на страницу авторизации
- На страницу можно перейти по прямому url. Например http://localhost:9000/table/case?caseUid=1234

Должно выполнятся! Дополнение MobX использовать в strict mode, то есть изменять состояние можно только через @action Для прокидывания MobX стейта, использовать Provider – из mobx-react, далее использовать во всех компонентах @inject(‘stateName’) Все интерфейсы должны быть описаны. Нельзя использовать тип any!!! То есть для всех аргументов, даже для событий мыши, нужно правильно использовать типы и правильно указывать обобщение. Тестовое задание должно запускаться при помощи двух команд. Yarn install / npm install. Yarn run start / npm start. Все красивости анимации на ваше усмотрение, но будет плюсом. Для создания элементов интерфейса можно использовать любые либы. Как вариант - https://material-ui.com/. Можно использовать любые boilerplate, для создания SPA. Почитайте о best practices по всему стеку, чтобы использовать наиболее элегантные решения.

## Дополнительное задание

Данное задание не обязательно выполнять, но необходимо знать, что в своей работе мы используем юнит тесты, поэтому надо знать и уметь их писать. Написать несколько юнит тестов. Использовать для этого библиотеку testing-library/react или enzyme.
