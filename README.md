# Тестовое задание для JavaScript FullStack разработчика

**ЦКП:** Учебная интеграция amoCRM с интерфейсом Vue и сервером NestJS по заданию ROCKET.

### Стек: VueJS + NestJS

---

# Описание задания

Необходимо разработать

-   API-приложение для доступа к сделкам и их контактам **amoCRM** (read-only)
-   Небольшое _представление,_ которое будет использовать данный API

## Backend

-   Приложение необходимо сделать на платформе [NodeJS](https://nodejs.org/en/), с использованием любого фреймворка c обязательным использованием **Typescript**
-   Разрабатываемому приложению будет достаточно одного GET-эндпоинта (например, `/api/leads`)
-   Эндпоинт по-умолчанию отдаёт все сделки и прикреплённые к ним контакты, но при наличии GET-параметра `query` (от трёх символов) отдача должна производиться с учётом фильтрации

    💡 **Подсказка**
    Не нужно изобретать свои алгоритмы фильтрации, воспользуйтесь [имеющимися возможностями amoCRM](https://www.amocrm.ru/developers/content/crm_platform/api-reference)

-   Разработанное API-приложение не подразумевает собственной авторизации/аутентификации, то есть backend должен возвращать ответ на любой "анонимный" запрос

## Frontend

-   Vue 3 (или React) c обязательным использованием **Typescript**
-   Желательно использовать UI-kit [Antd](https://www.antdv.com/) или любой
-   HTML-рендер можно осуществлять как на сервере, так и на клиенте (полный или частичный, в любых "пропорциях")
-   Главное - минимальный user-friendly интерфейс и чтобы ваше представление отображало всю необходимую информацию (как в [примере](#пример)).

## Подсказки

-   Демо-аккаунт  
    Для выполнения тестового задания необходим аккаунт в amoCRM, зарегистрировать демо-аккаунт можно [здесь](https://www.amocrm.ru/) (нажмите на кнопку "Пробная версия"), триал длится 14 дней, этого должно хватить

    -   Создание интеграции [https://skr.sh/sI6smeGtDJz?a](https://skr.sh/sI6smeGtDJz?a)

-   Упрощённая авторизация amoCRM (для запросов к API)  
    Для существенной экономии времени, при разработке приложения используйте [упрощённый способ авторизации](https://www.amocrm.ru/developers/content/oauth/easy-auth)
-   Фильтрация сущностей  
    Для фильтрации сущностей, используйте GET-параметр `query`. Этот параметр необходимо слать на ваше API-приложение, которое, в свою очередь, аналогично будет использовать его в качестве параметра при формировании запроса к API amoCRM
-   Статусы сделок  
    Чтобы узнать название воронки и статусов сделок, воспользуйтесь [данным методом](https://www.amocrm.ru/developers/content/crm_platform/leads_pipelines) API amoCRM
-   Ответственные менеджеры  
    Чтобы узнать имя ответственного менеджера, воспользуйтесь [данным методом](https://www.amocrm.ru/developers/content/crm_platform/users-api) API amoCRM

## Материалы

[Документация для разработчиков amoCRM](https://amocrm.ru/developers/content/crm_platform/api-reference)

-   [Упрощённая авторизация](https://www.amocrm.ru/developers/content/oauth/easy-auth)
-   [Сделки](https://www.amocrm.ru/developers/content/crm_platform/leads-api)
-   [Контакты](https://www.amocrm.ru/developers/content/api/recommendations)
-   [Воронки и этапы](https://www.amocrm.ru/developers/content/crm_platform/leads_pipelines)
-   [Пользователи](https://www.amocrm.ru/developers/content/crm_platform/users-api)
-   Оригинал задания в [Notion](https://rocketsales.notion.site/JavaScript-FullStack-1043991f7c9d4d56aec87237c5609477)

## Пример

Ознакомиться с примером работы можно [здесь](https://dev-test.rocketsales.ru/) (работает 24/7, но это не точно)
