# ULTRASILNYE — DevSecOps / Security Engineering Portfolio

Этот репозиторий — моя практическая база и портфолио для входа в информационную безопасность на роли:
- Junior Security Engineer
- Junior DevSecOps

Здесь я шаг за шагом строю и документирую безопасный инженерный процесс:
- автоматические проверки в GitHub Actions
- security gates
- анализ безопасности репозитория
- кейсы формата attack → fix → detect
- собственную knowledge base

---

## Что уже реализовано

На текущий момент в проекте уже работает:

- CI workflow в GitHub Actions
- Gitleaks — проверка на секреты
- Trivy — проверка на HIGH / CRITICAL уязвимости
- CodeQL — SAST-анализ
- Явно заданные минимальные permissions для workflow
- Knowledge Base с конспектом по Git, CI, security tools и GitHub Actions

---

## Где смотреть детали

- `notes/knowledge-base.md` — мой основной конспект и база знаний
- `notes/april-plan.md` — план действий до конца апреля
- `.github/workflows/ci.yml` — основной CI workflow
- `policies/` — правила и документы по security gates
- `reports/` — здесь будут оформленные кейсы
- `reports/case01_security_pipeline.md` — первый оформленный кейс по построению security pipeline

---

## Что я уже понял и отработал руками

В этом репозитории я уже прошёл через реальные этапы инженерной работы:

- создал и настроил GitHub-репозиторий
- включил автоматические security checks
- получил alert от CodeQL
- разобрал смысл замечания
- исправил workflow через `permissions: contents: read`
- зафиксировал изменения через commit и push
- оформил знания в собственную knowledge base
- оформил первый case-study в папке `reports`

---

## Roadmap

### Ближайшие шаги
- [x] Базовый CI
- [x] Secrets scanning (Gitleaks)
- [x] Vulnerability scanning (Trivy)
- [x] CodeQL / SAST
- [x] Knowledge Base
- [ ] Первый полноценный кейс в `reports/`
- [ ] README как витрина инженера
- [ ] Linux basics
- [ ] Docker basics
- [ ] Resume v1
- [ ] Первые отклики

---

## Зачем я веду этот репозиторий

Моя цель — не просто изучать теорию, а построить понятную и проверяемую инженерную базу, которую можно показать работодателю.

Этот репозиторий нужен мне как:
- подтверждение практики
- журнал роста
- фундамент для трудоустройства в ИБ