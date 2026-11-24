# Рабочий вес: сборка APK

Нужно: Node.js 18+ и Android Studio (с Android SDK).

1. В папке проекта:
   npm install
   npx cap add android
   npx @capacitor/assets generate --android
   npx cap sync android
2. Открыть в Android Studio:
   npx cap open android
3. Build > Build Bundle(s) / APK(s) > Build APK(s).
   Готовый файл: android/app/build/outputs/apk/debug/app-debug.apk

Установка на телефон: скопируйте APK и разрешите установку из неизвестных источников.
После правок в www/index.html выполните: npx cap sync android

## Сборка через GitHub (без Android Studio)
Загрузите содержимое этой папки в репозиторий GitHub. Вкладка Actions > Build APK > Run workflow.
Через несколько минут внизу страницы запуска появится файл rabochiy-ves-apk (внутри app-debug.apk).
