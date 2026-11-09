# ARNIX LAMPA ANDROID

Android-клиент Lampa на Kotlin. Проект использует WebView для выполнения оригинального JavaScript-интерфейса Lampa и её веб-плагинов, а Android-мост предоставляет ограниченные нативные функции.

## Сборка APK

APK собирается GitHub Actions при push в `main` или вручную через Actions → Build ARNIX LAMPA APK. Готовый APK будет доступен в Artifacts.

## Архитектура

- Kotlin + Android WebView
- JavaScript включён для работы приложения и совместимых веб-плагинов Lampa
- `ArnixBridge` — ограниченный JavaScript-мост Android
- Веб-интерфейс загружается с `https://lampa.mx`

Важно: это начальная оболочка Android, а не переписанный runtime Lampa. Полная совместимость со всеми сторонними плагинами и нативное воспроизведение через Media3 требуют отдельной интеграции и проверки.

## Сборка локально

Откройте проект в Android Studio и выполните сборку задачи `assembleDebug`.
