# Путеводитель: amoCRM-fullstack

Автономная инструкция: достаточно этой папки, исходников и перечисленных защищённых копий. История чатов и центральный каталог не требуются.

[Восстановление](RECOVERY.md) · [Карта файлов и зависимостей](PROJECT_MAP.json)

## Назначение

По [README.md](README.md): Не нужно изобретать свои алгоритмы фильтрации, воспользуйтесь имеющимися возможностями amoCRM

Обнаруженные языки: JavaScript, TypeScript, Vue SFC.

## Порядок чтения

1. Локальные AGENTS.md / CLAUDE.md и документы ниже.
2. Манифесты: версии среды, зависимости, команды.
3. Кандидаты точек входа; фактический запуск проверить по манифесту.
4. PROJECT_MAP.json: imports_local от источника к импортируемому файлу; входящие рёбра — потребители модуля.
5. RECOVERY.md: независимые данные, восстановление среды, запуск и критерии приёмки.

- [README.md](README.md)
- [client/README.md](client/README.md)
- [server/README.md](server/README.md)

## Манифесты

- [client/package.json](client/package.json)
- [server/package.json](server/package.json)

## Кандидаты точек входа

- [client/src/main.ts](client/src/main.ts)
- [server/src/main.ts](server/src/main.ts)

## Основные файлы по локальным импортам

| Файл | Входящих импортов |
|---|---:|
| [server/src/leads/leads.service.ts](server/src/leads/leads.service.ts) | 2 |
| [client/src/App.vue](client/src/App.vue) | 1 |
| [client/src/store/index.ts](client/src/store/index.ts) | 1 |
| [server/src/leads/leads.module.ts](server/src/leads/leads.module.ts) | 1 |
| [server/src/auth/auth.module.ts](server/src/auth/auth.module.ts) | 1 |
| [server/src/files/files.module.ts](server/src/files/files.module.ts) | 1 |
| [server/src/amo/amo.module.ts](server/src/amo/amo.module.ts) | 1 |
| [server/src/statuses/statuses.module.ts](server/src/statuses/statuses.module.ts) | 1 |
| [server/src/contacts/contacts.module.ts](server/src/contacts/contacts.module.ts) | 1 |
| [server/src/users/users.module.ts](server/src/users/users.module.ts) | 1 |
| [server/src/app.module.ts](server/src/app.module.ts) | 1 |
| [server/src/amo/amo.service.ts](server/src/amo/amo.service.ts) | 1 |

## Проверки


## Чтение карты без специальных плагинов

PROJECT_MAP.json — UTF-8 JSON: nodes и edges. Пути файлов относительные. contains обозначает наличие файла; imports_local — статически распознанный импорт; declares_dependency — объявление пакета в манифесте. evidence содержит источник и, где доступно, строку. Карта не исполняет код.

Статус исходного анализа: static-scan-complete; ограничений чтения: 0. Исходный снимок: 2026-10-30T14:47:11.360Z.

После изменения кода перечитайте затронутые файлы: карта является снимком. Отсутствие ребра не доказывает отсутствие зависимости.
