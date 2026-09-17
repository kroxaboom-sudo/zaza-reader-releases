# Skazka Hub 0.6.21-preview

> **RU — основной язык · EN — обязательный второй язык**

RU: Переходный выпуск Skazka Hub: новый публичный бренд, сохранённый путь обновления и более надёжная доставка служебных событий. Android 13+. EN: Transitional Skazka Hub release: new public brand, preserved upgrade path, and more reliable operational-event delivery. Android 13+.

## RU

Переходный выпуск Skazka Hub: новый публичный бренд, сохранённый путь обновления и более надёжная доставка служебных событий. Для Android 13 и новее.

- Публичное имя приложения теперь **Skazka Hub**; legacy `applicationId` сохранён, поэтому обновление устанавливается поверх Zaza Reader 0.6.20 без удаления приложения.
- Убрана пометка «тестовая версия» из стартового диалога; системное имя и уведомления используют Skazka Hub.
- Переходный updater сохраняет совместимость с текущим legacy release endpoint и подготовлен к будущему переименованию репозитория релизов.
- Повышена отказоустойчивость доставки диагностических и операционных событий Grouple: основной и резервные серверные маршруты работают независимо, а Telegram остаётся параллельным операционным каналом.
- Серверный release-gate проверил unit/integration tests, подпись APK и обновление **0.6.20 → 0.6.21** на Android 13 с сохранением данных приложения.

Минимальная версия: **Android 13 / API 33**. Обновление устанавливайте поверх существующей версии; удалять приложение не нужно.

> Примечание: полное покрытие интерфейса RU/EN относится к следующему этапу работ. Это описание уже приведено к новому обязательному формату RU/EN и не заявляет невыпущенные функции как реализованные.

## EN

This is a transitional Skazka Hub release: the new public brand is active, the existing upgrade path is preserved, and delivery of operational events is more resilient. Android 13 or newer is required.

- The public app name is now **Skazka Hub**. The legacy Android `applicationId` is preserved, so the update installs over Zaza Reader 0.6.20 without removing the app.
- The startup “test version” label was removed; system-facing app naming and notifications use Skazka Hub.
- The transitional updater remains compatible with the current legacy release endpoint and is prepared for the future release-repository rename.
- Grouple operational and diagnostic event delivery is more resilient: primary and fallback server routes operate independently, while Telegram remains a parallel operations channel.
- The server-side release gate verified unit/integration tests, APK signing and the **0.6.20 → 0.6.21** Android 13 upgrade while preserving app data.

Minimum version: **Android 13 / API 33**. Install this update over the existing app; do not uninstall first.

> Note: full RU/EN application UI coverage is part of the next development stage. This release description already follows the mandatory RU/EN documentation format without claiming unreleased features as implemented.
