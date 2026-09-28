🎬 LoockJson

A simple Android application for browsing popular movies and saving your favorite ones.

The application uses The Movie Database (TMDB) API to retrieve popular movies and displays their posters, titles, release dates and descriptions.

«Note: The repository is named "LooksJson", while the Android application itself is named "LoockJson".»

✨ Features

- 🎬 Browse popular movies
- 🖼️ Display movie posters
- 📖 View movie descriptions
- 📅 View release dates
- ❤️ Add movies to favorites
- ⭐ View saved favorite movies
- 💾 Store favorite movies locally using Room
- 🌐 Load movie data from TMDB API
- ⚡ Asynchronous operations with Kotlin Coroutines

🛠️ Tech Stack

- Kotlin
- Android SDK
- AndroidX
- Material Components
- Navigation Component
- ViewModel
- LiveData
- Room
- Retrofit
- Gson
- OkHttp
- Glide
- Kotlin Coroutines

🏗️ Architecture

The project separates the application into several layers:

app
├── data
│   ├── retrofit
│   │   └── api
│   │       ├── ApiService
│   │       └── RetrofitInstance
│   │
│   └── room
│       ├── dao
│       ├── repository
│       └── MoviesRoomDatabase
│
├── models
│   ├── MovieItemModel
│   └── MoviesModel
│
└── screens
    ├── main
    ├── detail
    └── favorite

Main screens

Main screen

Displays a list of popular movies loaded from TMDB.

Movie details

Shows:

- Movie poster
- Title
- Release date
- Description
- Favorite button

Favorites

Displays movies saved locally by the user.

🌐 API

Movie data is provided by The Movie Database (TMDB).

The application currently requests popular movies using the TMDB API.

GET /3/movie/popular

The API response is converted into Kotlin models using Retrofit and Gson.

Movie posters are loaded separately using Glide.

💾 Local Storage

Favorite movies are stored locally using Room Database.

The database contains a "movie_table" with information such as:

- "id"
- "title"
- "overview"
- "poster_path"
- "release_date"

This allows favorite movies to remain available without requesting them again from the API.

📱 Requirements

- Android Studio
- Android SDK
- JDK 8+
- Android device or emulator
- Internet connection

The current project configuration uses:

compileSdk 31
targetSdk 31
minSdk 23

🚀 Getting Started

Clone the repository:

git clone https://github.com/Nrskh/LooksJson.git

Open the project in Android Studio.

Allow Gradle to synchronize the project and then run the application on an Android device or emulator.

Alternatively, build the project from the command line:

Linux / macOS

./gradlew assembleDebug

Windows

gradlew.bat assembleDebug

The generated APK can be found in:

app/build/outputs/apk/debug/

🔑 TMDB API Key

The current project contains a TMDB API key directly in the API service configuration.

For a production application, it is recommended to avoid committing API keys to the repository and instead provide them through a secure configuration mechanism such as "local.properties", environment variables or Gradle secrets.

📂 Project Structure

src/
└── main/
    ├── java/
    │   └── com/afffundavbles/loockjson/
    │       ├── data/
    │       ├── models/
    │       ├── screens/
    │       ├── Const.kt
    │       ├── MainActivity.kt
    │       └── SaveShared.kt
    │
    └── res/
        ├── drawable/
        ├── layout/
        ├── menu/
        ├── navigation/
        ├── values/
        └── values-night/

🧪 Testing

The project includes unit and instrumentation test modules.

Run unit tests with:

./gradlew test

Run Android instrumentation tests with:

./gradlew connectedAndroidTest

📌 Current Status

The project is a small Android movie application demonstrating:

- REST API integration
- JSON parsing
- RecyclerView
- Navigation between fragments
- MVVM-style architecture
- Local persistence with Room
- Favorite movie management
- Image loading with Glide

🤝 Contributing

Contributions, improvements and bug fixes are welcome.

1. Fork the repository
2. Create a new branch

git checkout -b feature/my-feature

3. Make your changes
4. Commit your changes

git commit -m "Add my feature"

5. Push the branch

git push origin feature/my-feature

6. Open a Pull Request

📄 License

No license is currently specified for this repository.

If you intend to distribute or reuse the project, consider adding an appropriate open-source license.

👨‍💻 Author

Nrskh

GitHub: https://github.com/Nrskh





🎬 LoockJson

«Простое Android-приложение для просмотра популярных фильмов и добавления их в избранное.»

LoockJson — учебное Android-приложение на Kotlin, использующее API The Movie Database (TMDB) для получения информации о популярных фильмах.

Приложение позволяет просматривать фильмы, открывать подробную информацию о них и сохранять понравившиеся фильмы в избранное.

---

🇷🇺 Русский

✨ Возможности

- 🎬 Просмотр популярных фильмов
- 🖼️ Просмотр постеров
- 📖 Просмотр описания фильма
- 📅 Просмотр даты выхода
- ❤️ Добавление фильмов в избранное
- ⭐ Отдельный экран избранных фильмов
- 💾 Локальное сохранение избранного
- 🌐 Получение данных через TMDB API
- ⚡ Асинхронная работа с Kotlin Coroutines

🛠️ Используемые технологии

- Kotlin
- Android SDK
- AndroidX
- Material Components
- Navigation Component
- ViewModel
- LiveData
- Room
- Retrofit
- Gson
- OkHttp
- Glide
- Kotlin Coroutines

🏗️ Архитектура

Проект разделён на несколько основных частей:

src/main/java/com/afffundavbles/loockjson/

├── data/
│   ├── retrofit/
│   │   └── api/
│   │       ├── ApiService.kt
│   │       └── RetrofitInstance.kt
│   │
│   └── room/
│       ├── dao/
│       ├── repository/
│       └── MoviesRoomDatabase.kt
│
├── models/
│   ├── MovieItemModel.kt
│   └── MoviesModel.kt
│
├── screens/
│   ├── main/
│   ├── detail/
│   └── favorite/
│
├── MainActivity.kt
├── Const.kt
└── SaveShared.kt

📱 Основные экраны

Главный экран

Отображает список популярных фильмов, полученных через TMDB API.

Экран фильма

Показывает:

- постер;
- название;
- дату выхода;
- описание;
- статус избранного.

Избранное

Пользователь может добавлять фильмы в избранное и удалять их оттуда.

Избранные фильмы сохраняются локально с помощью Room Database.

🌐 TMDB API

Для получения информации о фильмах используется The Movie Database API.

Приложение получает список популярных фильмов:

GET /3/movie/popular

Данные API преобразуются в Kotlin-модели с помощью Retrofit + Gson.

Постеры фильмов загружаются с помощью Glide.

💾 Локальная база данных

Для хранения избранных фильмов используется Room.

Таблица "movie_table" содержит:

id
title
overview
poster_path
release_date

Благодаря этому избранные фильмы сохраняются на устройстве.

📋 Требования

- Android Studio
- Android SDK
- JDK 8+
- Android 6.0 (API 23) или выше
- Подключение к интернету

Текущая конфигурация проекта:

minSdk     23
compileSdk 31
targetSdk  31

🚀 Запуск проекта

Клонируйте репозиторий:

git clone https://github.com/Nrskh/LooksJson.git

Откройте проект в Android Studio и дождитесь синхронизации Gradle.

После этого запустите приложение на Android-устройстве или эмуляторе.

Для сборки APK:

Linux / macOS

./gradlew assembleDebug

Windows

gradlew.bat assembleDebug

APK будет находиться в:

app/build/outputs/apk/debug/

🔑 TMDB API Key

В текущей версии проекта API-ключ TMDB находится непосредственно в "ApiService.kt".

Для production-приложения рекомендуется не хранить API-ключ непосредственно в исходном коде, а использовать "local.properties", переменные окружения или другой безопасный способ конфигурации.

🧪 Тестирование

Запуск unit-тестов:

./gradlew test

Запуск Android instrumentation tests:

./gradlew connectedAndroidTest

🤝 Участие в разработке

Будем рады предложениям, исправлениям и улучшениям.

1. Сделайте Fork репозитория.
2. Создайте новую ветку:

git checkout -b feature/my-feature

3. Внесите изменения.
4. Создайте commit:

git commit -m "Add my feature"

5. Отправьте ветку:

git push origin feature/my-feature

6. Создайте Pull Request.

📄 Лицензия

На данный момент отдельная open-source лицензия в проекте не указана.

---

🇰🇿 Қазақша

«Танымал фильмдерді көруге және ұнаған фильмдерді таңдаулыларға қосуға арналған қарапайым Android қолданбасы.»

LoockJson — Kotlin тілінде жасалған оқу мақсатындағы Android қолданбасы. Қолданба фильмдер туралы ақпарат алу үшін The Movie Database (TMDB) API пайдаланады.

Қолданба арқылы танымал фильмдерді көруге, фильм туралы толық ақпаратты ашуға және ұнаған фильмдерді таңдаулыларға сақтауға болады.

---

✨ Мүмкіндіктері

- 🎬 Танымал фильмдерді көру
- 🖼️ Фильм постерлерін көру
- 📖 Фильм сипаттамасын оқу
- 📅 Шыққан күнін көру
- ❤️ Фильмді таңдаулыларға қосу
- ⭐ Таңдаулы фильмдердің жеке бөлімі
- 💾 Таңдаулы фильмдерді құрылғыда сақтау
- 🌐 TMDB API арқылы деректер алу
- ⚡ Kotlin Coroutines арқылы асинхронды жұмыс

🛠️ Қолданылған технологиялар

- Kotlin
- Android SDK
- AndroidX
- Material Components
- Navigation Component
- ViewModel
- LiveData
- Room
- Retrofit
- Gson
- OkHttp
- Glide
- Kotlin Coroutines

🏗️ Жоба құрылымы

src/main/java/com/afffundavbles/loockjson/

├── data/
│   ├── retrofit/
│   │   └── api/
│   │       ├── ApiService.kt
│   │       └── RetrofitInstance.kt
│   │
│   └── room/
│       ├── dao/
│       ├── repository/
│       └── MoviesRoomDatabase.kt
│
├── models/
│   ├── MovieItemModel.kt
│   └── MoviesModel.kt
│
├── screens/
│   ├── main/
│   ├── detail/
│   └── favorite/
│
├── MainActivity.kt
├── Const.kt
└── SaveShared.kt

📱 Негізгі экрандар

Басты экран

TMDB API арқылы алынған танымал фильмдердің тізімін көрсетеді.

Фильм туралы ақпарат

Фильмнің:

- постері;
- атауы;
- шыққан күні;
- сипаттамасы;
- таңдаулы күйі көрсетіледі.

Таңдаулылар

Пайдаланушы ұнаған фильмдерді таңдаулыларға қоса алады немесе оларды тізімнен өшіре алады.

Таңдаулы фильмдер Room Database арқылы құрылғыда жергілікті сақталады.

🌐 TMDB API

Фильмдер туралы ақпарат алу үшін The Movie Database API қолданылады.

Қолданба танымал фильмдерді келесі endpoint арқылы алады:

GET /3/movie/popular

API-дан келген JSON деректері Retrofit + Gson арқылы Kotlin модельдеріне түрлендіріледі.

Фильм постерлері Glide кітапханасы арқылы жүктеледі.

💾 Жергілікті деректер базасы

Таңдаулы фильмдерді сақтау үшін Room Database пайдаланылады.

"movie_table" кестесінде келесі мәліметтер сақталады:

id
title
overview
poster_path
release_date

Осының арқасында таңдаулы фильмдер құрылғыда сақталып қалады.

📋 Қажетті талаптар

- Android Studio
- Android SDK
- JDK 8+
- Android 6.0 (API 23) немесе одан жоғары
- Интернет байланысы

Жобаның қазіргі конфигурациясы:

minSdk     23
compileSdk 31
targetSdk  31

🚀 Жобаны іске қосу

Репозиторийді клондатыңыз:

git clone https://github.com/Nrskh/LooksJson.git

Жобаны Android Studio арқылы ашып, Gradle синхронизациясының аяқталуын күтіңіз.

Содан кейін қолданбаны Android құрылғысында немесе эмуляторда іске қосуға болады.

APK құрастыру:

Linux / macOS

./gradlew assembleDebug

Windows

gradlew.bat assembleDebug

Дайын APK мына жерде орналасады:

app/build/outputs/apk/debug/

🔑 TMDB API Key

Қазіргі нұсқада TMDB API кілті "ApiService.kt" файлының ішінде орналасқан.

Production қолданбасында API кілтін бастапқы кодта тікелей сақтамаған дұрыс. Оның орнына "local.properties", environment variables немесе басқа қауіпсіз конфигурация әдісін қолдану ұсынылады.

🧪 Тестілеу

Unit-тесттерді іске қосу:

./gradlew test

Android instrumentation тесттерін іске қосу:

./gradlew connectedAndroidTest

🤝 Жобаға үлес қосу

Жобаға ұсыныстар, түзетулер және жаңа мүмкіндіктер қосуға болады.

1. Репозиторийге Fork жасаңыз.
2. Жаңа branch құрыңыз:

git checkout -b feature/my-feature

3. Өзгерістер енгізіңіз.
4. Commit жасаңыз:

git commit -m "Add my feature"

5. Branch-ті GitHub-қа жіберіңіз:

git push origin feature/my-feature

6. Pull Request ашыңыз.

📄 Лицензия

Қазіргі уақытта репозиторийде жеке open-source лицензия көрсетілмеген.
