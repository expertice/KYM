# Contributing to К.У.М.

Спасибо за вклад. На этапе bootstrap приоритет — документация, ADR и безопасный Git-workflow. Бизнес-функции добавляются только по согласованному плану.

## Перед началом

1. Прочитай [README.md](README.md) и [docs/product/](docs/product/README.md).
2. Сверься с [docs/architecture/](docs/architecture/README.md) и актуальными [ADR](docs/adr/README.md).
3. Для агентов Cursor действуют правила в `.cursor/rules/`.

## Workflow

1. Создай ветку от актуального `main` (или базовой ветки команды):
   - `docs/...` — документация/ADR
   - `feat/...` — функциональность
   - `fix/...` — исправления
   - `chore/...` — инфраструктура/инструменты
2. Внеси изменения минимальным диффом.
3. Обнови документацию и CHANGELOG, если поведение/архитектура меняются.
4. Открой PR по шаблону `.github/PULL_REQUEST_TEMPLATE.md`.

## Conventional Commits

Формат:

```text
<type>(optional-scope): <summary>
```

Типы: `feat`, `fix`, `docs`, `chore`, `test`, `refactor`, `ci`, `build`, `perf`.

Примеры:

```text
docs: add ADR-0006 for persistence of world tree
fix(simulation): reject client-authored simulation results
chore: add Unity .gitignore entries
```

## Тесты

- Новый behaviour — с тестом в том же PR (когда появится test harness).
- Обязательные инварианты: дерево миров, optimistic concurrency, audit, серверная симуляция.
- Не коммитьте красные тесты как норму.

## Документация и ADR

- Архитектурно значимое решение → новый или обновлённый ADR в `docs/adr/`.
- Краткая запись → `docs/decisions/`.
- Операционные шаги → `docs/runbooks/`.
- Контракты → `docs/api/` и `docs/model-schemas/`.

## Безопасность Git

- Не коммитьте секреты, `.env`, ключи, токены.
- Не используйте `push --force` в `main` / `master`.
- Не отключайте hooks (`--no-verify`) без явного согласования.
- Коммиты и push — осознанно; force/hard reset — только по явной необходимости и согласованию.

## Code review

PR должен отвечать:

- зачем изменение;
- какие ADR/docs затронуты;
- как проверить;
- какие риски.

Ревьюер проверяет соответствие ADR-0001…0005 и правилам в `.cursor/rules/`.
