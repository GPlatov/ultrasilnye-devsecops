# Case 01 — Security Pipeline for GitHub Repository

## 1. Контекст
Я создаю GitHub-репозиторий как практическое портфолио для перехода в информационную безопасность на роль Junior Security Engineer с DevSecOps-уклоном.

Цель репозитория:
- вести knowledge base
- строить инженерный security pipeline
- оформлять практические кейсы
- показать работодателю реальную работу руками

---

## 2. Что было сделано
В репозитории были настроены и подключены:

- Git и GitHub как основа хранения и истории изменений
- CI workflow через GitHub Actions
- Gitleaks для поиска секретов
- Trivy для поиска уязвимостей
- CodeQL для SAST-анализа
- Dependabot для обновлений GitHub Actions
- Knowledge Base для фиксации понимания и практики

---

## 3. Что проверяет мой pipeline
### Gitleaks
Ищет секреты:
- токены
- ключи
- пароли
- чувствительные строки

### Trivy
Ищет уязвимости:
- HIGH
- CRITICAL
- опасные зависимости и проблемы в проекте

### CodeQL
Ищет потенциально опасные места в коде и конфигурации.
Показывает security alerts во вкладке Security.

---

## 4. Реальный security alert
Во время анализа CodeQL был найден alert:

`Workflow does not contain permissions`

Смысл замечания:
в workflow не были явно заданы permissions, из-за чего права могли быть шире, чем реально нужны.

---

## 5. Как я исправил проблему
Я открыл файл `.github/workflows/ci.yml` и добавил блок:

```yaml
permissions:
  contents: read