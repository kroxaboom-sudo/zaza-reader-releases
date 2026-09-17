<p align="center">
  <img src="assets/banner.svg" alt="Skazka Hub" width="960">
</p>

<p align="center">
  <a href="https://github.com/kroxaboom-sudo/zaza-reader-releases/releases/latest"><img src="https://img.shields.io/github/v/release/kroxaboom-sudo/zaza-reader-releases?label=Latest&cacheSeconds=300" alt="Latest release"></a>
  <img src="https://img.shields.io/badge/Android-13%2B-3DDC84" alt="Android 13+">
  <img src="https://img.shields.io/badge/languages-RU%20%2F%20EN-blue" alt="RU / EN">
</p>

# Skazka Hub — releases / релизы

> **RU — основной язык · EN — обязательный второй язык**

## RU

**Skazka Hub** — Android-приложение для чтения с локальной/offline-first библиотекой. Текущий публично поддерживаемый источник — **a.zazaza.me**; архитектура проекта предусматривает подключение дополнительных источников через Grouple Registry после проверки.

### Текущий публичный выпуск

- **Skazka Hub v0.6.21-preview**.
- Минимальная версия: **Android 13 / API 33**.
- Это переходный выпуск после Zaza Reader: публичное имя уже **Skazka Hub**, а legacy `applicationId` / package сохранён для установки обновления поверх предыдущей версии без удаления приложения.
- Старые APK Zaza Reader остаются в истории как часть совместимого пути обновления.

Скачать актуальный APK: **Releases → Latest**. Для обновления устанавливайте новую версию поверх существующей.

### Что является текущей архитектурой проекта

- **Local-first / offline-first:** сохранённая библиотека, локальные метаданные, прогресс и загруженный контент не должны зависеть от постоянной доступности сервера.
- **SERVER-FIRST:** собственный HOSTKEY — основная площадка для серверной логики, тестов, release-gate, health-check, Telegram-интеграций и эксплуатационных задач.
- **GitHub минимально:** репозитории, история, теги и публичные Releases; GitHub Actions не должен быть обязательным runtime-звеном проекта.
- **APP / CFG / REG / SRV / OPS:** APK, удалённая конфигурация, Registry, сервер и эксплуатационный слой версионируются независимо.
- Обновления **CFG/REG/SRV/OPS** могут распространяться без нового APK; персональные уведомления об APK и no-APK изменениях предусмотрены через Telegram.
- **Direct** — основной маршрут к источникам; **VPN/Proxy** — резерв и диагностический маршрут.
- **Vercel** сохраняется как отключаемый резервный модуль и не является обязательной зависимостью.
- Основные функции приложения не должны требовать платной серверной инфраструктуры.

### Что сейчас находится в работе

Текущий критический путь разработки:

1. единая система Downloads для **IMAGE + TEXT**;
2. **SQLite / LocalState + Library v2**;
3. offline/sync и единый Download Manager;
4. цепочка TEXT → библиотека → Reader;
5. updater и проверка бесшовного обновления;
6. завершение миграции бренда **Zaza Reader → Skazka Hub** и последующее переименование репозиториев в утверждённой точке;
7. полная локализация **RU/EN** интерфейсов, служебных текстов, описаний и release notes;
8. финальный релизный аудит: подпись, сохранность данных, endpoints, HOSTKEY, Telegram/Control Panel и соблюдение правила проекта «всё своё».

Запланированные функции в этом разделе не следует считать уже присутствующими в опубликованном APK, пока они не указаны в release notes конкретной версии.

### Репозиторий

Этот публичный репозиторий содержит APK, файлы встроенного обновления и пользовательские release notes. Исходный Android-код хранится отдельно в приватном репозитории. Ключ подписи APK не публикуется.

Текущее имя репозитория `zaza-reader-releases` является legacy-именем и будет изменено в утверждённой точке полной миграции, без разрыва существующего update path.

---

## EN

**Skazka Hub** is an Android reader built around a local-first/offline-first library. The currently supported public source is **a.zazaza.me**; the architecture is designed to add more verified sources through Grouple Registry later.

### Current public release

- **Skazka Hub v0.6.21-preview**.
- Minimum Android version: **Android 13 / API 33**.
- This is a transition release from Zaza Reader: the public product name is already **Skazka Hub**, while the legacy Android `applicationId` / package is preserved for seamless upgrades without removing the app.
- Historical Zaza Reader APKs remain available as part of the compatible upgrade history.

Use **Releases → Latest** for the current APK and install updates over the existing app.

### Current project architecture

- **Local-first / offline-first:** saved library data, local metadata, reading progress and downloaded content must remain usable without continuous server availability.
- **SERVER-FIRST:** the project-owned HOSTKEY server is the primary environment for backend logic, tests, release gates, health checks, Telegram integrations and operations.
- **Minimal GitHub dependency:** source/history/tags/public Releases; GitHub Actions must not become a required runtime dependency.
- Independent version tracks: **APP / CFG / REG / SRV / OPS**.
- **CFG/REG/SRV/OPS** may be updated without a new APK; Telegram notifications cover both APK and no-APK changes.
- **Direct** source access is primary; **VPN/Proxy** is a resilience and diagnostic fallback.
- **Vercel** is retained only as an optional/disableable module, not a mandatory dependency.
- Core app functionality must not require paid server infrastructure.

### Current development path

1. unified **IMAGE + TEXT** Downloads;
2. **SQLite / LocalState + Library v2**;
3. offline/sync and unified Download Manager;
4. TEXT → library → Reader flow;
5. updater and seamless-upgrade verification;
6. complete **Zaza Reader → Skazka Hub** migration and repository rename at the approved migration point;
7. complete **RU/EN** coverage for UI, service text, descriptions and release notes;
8. final release audit covering signing, user-data continuity, endpoints, HOSTKEY, Telegram/Control Panel and the project’s own-code rule.

Items in the roadmap are not claimed as present in the current APK unless the release notes for that version explicitly say so.

### Repository role

This public repository contains APK files, in-app update metadata and user-facing release notes. Android source code is stored separately in a private repository. APK signing keys are never published.

The repository name `zaza-reader-releases` is a legacy compatibility name and is planned to change at the approved full-migration point without breaking the existing update path.
