# NestJS + express-handlebars

Пример использования express-handlebars в качестве шаблонизатора в NestJS.

## Стек технологий

- **Runtime**: Node.js (>= 14)
- **Язык**: TypeScript 4
- **Фреймворк**: NestJS 7
- **Шаблонизатор**: express-handlebars 5
- **Тестирование**: Jest, Supertest
- **Линтер**: ESLint (с @typescript-eslint)
- **Форматирование**: Prettier

## Установка

```bash
npm install
```

## Запуск

### Режим разработки (с hot-reload)

```bash
npm run start:dev
```

Приложение будет доступно по адресу http://localhost:3000.

### Production сборка

```bash
npm run build
npm run start:prod
```

### Режим отладки

```bash
npm run start:debug
```

## Тестирование

```bash
# unit-тесты
npm run test

# unit-тесты в режиме watch
npm run test:watch

# coverage
npm run test:cov

# e2e-тесты
npm run test:e2e
```

## Линтинг и форматирование

```bash
# линтинг
npm run lint

# форматирование
npm run format
```

## Маршруты

| Маршрут | Описание |
|---------|----------|
| `/` | Базовая страница с приветствием |
| `/name` | Пример использования helper-функции |
| `/layout` | Пример смены layout |
| `/array` | Пример отображения массива |

## Структура проекта

```
src/
├── main.ts           # Точка входа, настройка шаблонизатора
├── app.module.ts     # Корневой модуль
├── app.controller.ts # Контроллер с маршрутами
├── app.service.ts    # Сервис
└── hbs/
    └── helpers.ts    # Handlebars helpers

views/
├── layouts/          # Layouts (main, other)
├── partials/         # Partials (navbar, footer)
├── index.hbs         # Главная страница
├── print.hbs         # Страница с helper
├── array.hbs         # Страница с массивом
└── alpine/           # Примеры с Alpine.js
```

## Особенности

- Используются layouts, partials и кастомные helpers express-handlebars
- Все маршруты в одном контроллере для наглядности

## Лицензия

ISC © 2021 AudiBookning
