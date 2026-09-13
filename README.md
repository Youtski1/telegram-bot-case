# Коммерческий Telegram-бот (закрытый код)

## Задача

Написать бота с функционалом:

- 📢 Пиар чатов
- 🛡️ Модерация чатов
- 🎮 Встроенные игры (игры для вовлечения участников чата)
- 🧬 Копии основного бота (создание дочерних ботов с собственными настройками)
- ⚙️ Настройки чата

## Стек

**Bot Service:**
- Python 3.11+
- Aiogram 3.x
- SQLAlchemy 2.0 (async)
- Alembic (миграции)
- PostgreSQL
- PyTest (unit + integration)

**API Service:**
- TypeScript
- Express
- Drizzle ORM
- PostgreSQL
- Docker

Реализованы тесты для 60–70% кода.

## Архитектура проекта

Проект состоит из двух микросервисов, работающих через Docker Compose.

### Структура

```text
├── api_service
│   ├── DockerFile
│   ├── drizzle.config.ts
│   ├── package.json
│   ├── package-lock.json
│   ├── src
│   │   ├── api
│   │   │   ├── config.ts
│   │   │   ├── controllers
│   │   │   ├── dockerClient.ts
│   │   │   ├── factory
│   │   │   ├── index.ts
│   │   │   ├── logger.ts
│   │   │   ├── manager_api.ts
│   │   │   ├── middlewaries
│   │   │   ├── repositories
│   │   │   ├── routers
│   │   │   ├── services
│   │   │   ├── types
│   │   │   └── utils
│   │   └── database
│   │       ├── db.ts
│   │       └── migrations
│   └── tsconfig.json
├── bot_service
│   ├── alembic.ini
│   ├── DockerFile
│   ├── pytest.ini
│   ├── requirements.txt
│   ├── src
│   │   ├── bot
│   │   │   ├── config.py
│   │   │   ├── container.py
│   │   │   ├── kbs.py
│   │   │   ├── main.py
│   │   │   ├── middlewares
│   │   │   ├── paginations
│   │   │   ├── repositories
│   │   │   ├── routers
│   │   │   ├── services
│   │   │   ├── states
│   │   │   ├── text_storage
│   │   │   ├── types
│   │   │   └── utils
│   │   ├── checkers_database
│   │   │   ├── checker_restrictions
│   │   │   └── checker_timer_entities_piar
│   │   ├── database
│   │   │   ├── custom_types.py
│   │   │   ├── db_helper.py
│   │   │   ├── db.py
│   │   │   ├── migrations
│   │   │   └── models
│   │   └── logging
│   │       ├── colored_formatter.py
│   │       ├── init.py
│   │       ├── logging_config.yaml
│   │       └── logging_setup.py
│   └── tests
│       ├── conftest.py
│       ├── integration
│       │   ├── test_checkers
│       │   ├── test_modular_services
│       │   ├── test_repositories
│       │   └── test_services
│       └── unit
│           ├── filter_link_service_test.py
│           ├── search_argument_test.py
│           ├── search_time_test.py
│           └── test_services
├── docker-compose.yaml
├── package.json
├── package-lock.json
└── tz.txt
```

41 directories, 34 files

## Результат

Бюджет: 90 000 ₽.

## Код

Код находится в закрытом репозитории (по договору с заказчиком).
Бот в телеграм t.me/@Clevercheak_bot
