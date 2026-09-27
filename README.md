# К.У.М. — Конструктор управленческих моделей

Платформа для проектирования, **серверной симуляции** и анализа управленческих моделей во **вложенных мирах**.

> Сейчас в репозитории — документационный и процессный bootstrap. Бизнес-функции продукта ещё не реализованы.

## Быстрый старт

Локальный запуск приложения **пока недоступен**: нет backend/Unity-проекта и Docker Compose.

После появления runtime ожидаемые шаги будут описаны в:

- [docs/runbooks/](docs/runbooks/README.md)
- этом README (секция будет обновлена)

## Документация

| Раздел | Путь |
|--------|------|
| Продукт | [docs/product/](docs/product/README.md) |
| Архитектура | [docs/architecture/](docs/architecture/README.md) |
| ADR | [docs/adr/](docs/adr/README.md) |
| API | [docs/api/](docs/api/README.md) |
| Схемы моделей | [docs/model-schemas/](docs/model-schemas/README.md) |
| Runbooks | [docs/runbooks/](docs/runbooks/README.md) |
| Decisions log | [docs/decisions/](docs/decisions/README.md) |

## Архитектурные опоры (кратко)

1. **Модульный монолит** — один backend deployable, жёсткие границы модулей.
2. **Unity WebGL** — клиент визуализации; не источник истины.
3. **Серверная симуляция** — канонические результаты только на сервере.
4. **Миры как дерево** — иерархия без циклов.
5. **Optimistic concurrency + audit** — версии при мутациях и append-only след изменений.

Подробности — в [docs/adr/](docs/adr/README.md).

## Участие

См. [CONTRIBUTING.md](CONTRIBUTING.md). Правила для агентов Cursor — в [`.cursor/rules/`](.cursor/rules/).

## Changelog

См. [CHANGELOG.md](CHANGELOG.md).

## Лицензия

Лицензия будет добавлена отдельным решением владельцев репозитория.
