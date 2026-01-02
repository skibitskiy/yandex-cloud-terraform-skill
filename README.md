# Yandex Cloud Terraform Plugin

Claude Code plugin для работы с Terraform и Yandex Cloud. Предоставляет паттерны инфраструктуры как кода, соглашения по именованию и лучшие практики для serverless-сервисов Yandex Cloud.

## Возможности

- **YDB** — создание таблиц, TTL, вторичные индексы
- **Cloud Functions** — сборка и деплой функций
- **Message Queue** — DLQ и паттерны повторных попыток
- **Serverless Containers** — Docker registry, триггеры, конфигурация ресурсов
- **IAM** — типовые комбинации ролей и сервисные аккаунты

## Установка

### Локально (для разработки)

```bash
claude --plugin-dir /path/to/yandex-cloud-terraform-skill
```

### Через marketplace

Если плагин опубликован в marketplace:

```bash
claude plugin install yandex-cloud-terraform
```

### Вручную

Скопируйте плагин в директорию плагинов Claude Code:

```bash
# macOS / Linux
cp -r /path/to/yandex-cloud-terraform-skill ~/.claude/plugins/yandex-cloud-terraform

# Windows
xcopy /E /I \\path\\to\\yandex-cloud-terraform-skill %USERPROFILE%\.claude\plugins\yandex-cloud-terraform
```

## Использование

После установки Claude Code автоматически применяет паттерны из этого плагина при работе с Terraform-конфигурациями для Yandex Cloud.

Примеры запросов:
- "Создай YDB таблицу с TTL"
- "Добавь Cloud Function с триггером из Message Queue"
- "Настрой Serverless Container с Docker registry"

## Структура

```
.
├── .claude-plugin/
│   └── plugin.json                 # Манифест плагина
├── skills/
│   └── yandex-cloud-terraform/
│       ├── SKILL.md                # Основной файл skill
│       └── references/
│           ├── CONTAINERS.md       # Serverless Containers
│           ├── FUNCTIONS.md        # Cloud Functions
│           ├── IAM.md              # IAM роли и сервисные аккаунты
│           ├── QUEUE.md            # Message Queue
│           └── YDB.md              # Yandex Database
└── README.md
```

## Лицензия

MIT
