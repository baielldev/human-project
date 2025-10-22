# Git Flow

## 1️⃣ Git Branch Naming

- `main` — Продакшн
- `dev` — Тестируемая и разрабатываемая ветка
- `feature/*` — Новая фича
- `hotfix/*` — Исправление критических проблем
- `bugfix/*` — Исправление багов

## 2️⃣ Порядок работы с ветками через git flow

### Шаг 1: Переключение на dev ветку

```bash
git checkout dev
```

### Шаг 2: Инициализация работы фичи

```bash
git flow feature start header-block
```

### Шаг 3: Работа над фичей и коммиты

```bash
git add .
git commit -m "Добавил блок header"
```

### Шаг 4: Завершение работы фичи

```bash
git flow feature finish header-block
```

### Шаг 5: Пуш изменений на продакшн

```bash
git push -u origin dev
git checkout main
git pull origin dev
git push -u origin main
```

**‼️‼️‼️После того как работа над блоком была закончена, обязательно упомянуть об этом и проверить, были ли запушены изменения, чтобы не возникло конфликтов.‼️‼️‼️**

## 3️⃣ Команды через git flow

- Создание ветки: `git flow [branch] start [branch_name]`
- Завершение ветки: `git flow [branch] finish [branch_name]`

Пример:

```bash
git flow feature finish header-block
```
