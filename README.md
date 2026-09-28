🎬 LoockJson

Android-приложение для просмотра популярных фильмов с использованием The Movie Database (TMDB) API.
Приложение позволяет получать список фильмов из API, просматривать подробную информацию и сохранять фильмы в избранное.

---

🇷🇺 Русский

📱 О проекте

LoockJson — Android-приложение на Kotlin для работы с фильмами через TMDB API.

Приложение получает список популярных фильмов из TMDB, отображает постеры и основную информацию о фильмах. Пользователь может открыть страницу фильма и добавить его в избранное.

✨ Возможности

- 🎬 Получение популярных фильмов через TMDB API
- 🖼️ Отображение постеров фильмов
- 📄 Просмотр подробной информации:
  - название
  - дата выхода
  - описание
  - постер
- ❤️ Добавление и удаление фильмов из избранного
- 💾 Локальное хранение избранных фильмов
- 🌐 Работа с REST API
- 🔄 Асинхронные запросы с использованием Kotlin Coroutines

🛠️ Технологии

- Kotlin
- Android SDK
- AndroidX
- Material Components
- Retrofit
- OkHttp
- Gson
- Kotlin Coroutines
- Room Database
- Glide
- ViewModel
- Navigation Component

🏗️ Архитектура проекта

LooksJson/
├── .gitignore
├── README.md
├── build.gradle
├── gradle.properties
├── gradlew
├── gradlew.bat
├── local.properties
├── proguard-rules.pro
├── settings.gradle
│
├── gradle/
│   └── wrapper/
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
│
└── src/
    ├── main/
    │   ├── AndroidManifest.xml
    │   │
    │   ├── java/
    │   │   └── com/
    │   │       └── afffundavbles/
    │   │           └── loockjson/
    │   │               ├── Const.kt
    │   │               ├── MainActivity.kt
    │   │               ├── SaveShared.kt
    │   │               │
    │   │               ├── data/
    │   │               │   ├── retrofit/
    │   │               │   │   ├── RetrofitRepository.kt
    │   │               │   │   └── api/
    │   │               │   │       ├── ApiService.kt
    │   │               │   │       └── RetrofitInstance.kt
    │   │               │   │
    │   │               │   └── room/
    │   │               │       ├── MoviesRoomDatabase.kt
    │   │               │       ├── dao/
    │   │               │       │   └── MoviesDao.kt
    │   │               │       └── repository/
    │   │               │           ├── MoviesRepository.kt
    │   │               │           └── MoviesRepositoryRealization.kt
    │   │               │
    │   │               ├── models/
    │   │               │   ├── MovieItemModel.kt
    │   │               │   └── MoviesModel.kt
    │   │               │
    │   │               └── screens/
    │   │                   ├── detail/
    │   │                   │   ├── DetailFragment.kt
    │   │                   │   └── DetailViewModel.kt
    │   │                   │
    │   │                   ├── favorite/
    │   │                   │   ├── FavoriteAdapter.kt
    │   │                   │   ├── FavoriteFragment.kt
    │   │                   │   └── FavoriteFragmentViewModel.kt
    │   │                   │
    │   │                   └── main/
    │   │                       ├── MainAdapter.kt
    │   │                       ├── MainFragment.kt
    │   │                       └── MainFragmentViewModel.kt
    │   │
    │   └── res/
    │       ├── drawable/
    │       │   ├── ic_baseline_favorite_24.xml
    │       │   ├── ic_baseline_favorite_border_24.xml
    │       │   └── ic_launcher_background.xml
    │       │
    │       ├── drawable-v24/
    │       │   └── ic_launcher_foreground.xml
    │       │
    │       ├── layout/
    │       │   ├── activity_main.xml
    │       │   ├── fragment_detail.xml
    │       │   ├── fragment_favorite.xml
    │       │   ├── fragment_main.xml
    │       │   └── item_layout.xml
    │       │
    │       ├── menu/
    │       │   └── main_menu.xml
    │       │
    │       ├── navigation/
    │       │   └── nav_graph.xml
    │       │
    │       ├── mipmap-anydpi-v26/
    │       │   ├── ic_launcher.xml
    │       │   └── ic_launcher_round.xml
    │       │
    │       ├── mipmap-hdpi/
    │       │   ├── ic_launcher.webp
    │       │   └── ic_launcher_round.webp
    │       │
    │       ├── mipmap-mdpi/
    │       │   ├── ic_launcher.webp
    │       │   └── ic_launcher_round.webp
    │       │
    │       ├── mipmap-xhdpi/
    │       │   ├── ic_launcher.webp
    │       │   └── ic_launcher_round.webp
    │       │
    │       ├── mipmap-xxhdpi/
    │       │   ├── ic_launcher.webp
    │       │   └── ic_launcher_round.webp
    │       │
    │       ├── mipmap-xxxhdpi/
    │       │   ├── ic_launcher.webp
    │       │   └── ic_launcher_round.webp
    │       │
    │       ├── values/
    │       │   ├── colors.xml
    │       │   ├── strings.xml
    │       │   └── themes.xml
    │       │
    │       └── values-night/
    │           └── themes.xml
    │
    ├── androidTest/
    │   └── java/
    │       └── com/
    │           └── afffundavbles/
    │               └── loockjson/
    │                   └── ExampleInstrumentedTest.kt
    │
    └── test/
        └── java/
            └── com/
                └── afffundavbles/
                    └── loockjson/
                        └── ExampleUnitTest.kt
                        ```text

🖥️ Экраны

Главный экран

Отображает список популярных фильмов, полученных через TMDB API.

Экран фильма

Показывает:

- название фильма;
- дату выхода;
- описание;
- постер;
- возможность добавить фильм в избранное.

Избранное

Содержит фильмы, которые пользователь сохранил локально.

🌐 TMDB API

Приложение использует API сервиса The Movie Database (TMDB) для получения информации о фильмах.

Базовый URL:

https://api.themoviedb.org/

Используемый endpoint:

GET /3/movie/popular

Для работы приложения необходим API-ключ TMDB.

«⚠️ В текущей версии проекта API-ключ находится непосредственно в исходном коде. Для production-версии рекомендуется вынести ключ в "local.properties", "BuildConfig" или другой безопасный механизм конфигурации и не публиковать его в Git.»

💾 Локальная база данных

Для хранения избранных фильмов используется Room Database.

Данные сохраняются локально, поэтому избранные фильмы доступны без повторного запроса к TMDB для их хранения.

📋 Требования

- Android Studio
- JDK 8+
- Android SDK
- Android 6.0 (API 23) или выше
- API Key от TMDB

🚀 Запуск проекта

1. Клонируйте репозиторий:

git clone https://github.com/Nrskh/LooksJson.git

2. Откройте проект в Android Studio.

3. Добавьте API-ключ TMDB в конфигурацию проекта.

4. Синхронизируйте Gradle.

5. Запустите приложение на эмуляторе или Android-устройстве.

🧪 Тестирование

В проекте присутствуют:

- Unit-тесты
- Instrumented-тесты

Запуск тестов:

./gradlew test

Для Windows:

gradlew.bat test

📄 Лицензия

На данный момент отдельная лицензия в проекте не указана.

---

🇰🇿 Қазақша

📱 Жоба туралы

LoockJson — фильмдер туралы ақпаратты The Movie Database (TMDB) API арқылы алуға арналған Android қосымшасы.

Қосымша TMDB сервисінен танымал фильмдердің тізімін алады, олардың постерлері мен негізгі ақпаратын көрсетеді. Пайдаланушы фильмнің толық ақпаратын көріп, оны таңдаулыларға қоса алады.

✨ Мүмкіндіктері

- 🎬 TMDB API арқылы танымал фильмдерді алу
- 🖼️ Фильмдердің постерлерін көрсету
- 📄 Фильм туралы толық ақпаратты көру:
  - атауы
  - шығу күні
  - сипаттамасы
  - постері
- ❤️ Фильмдерді таңдаулыларға қосу және өшіру
- 💾 Таңдаулы фильмдерді жергілікті сақтау
- 🌐 REST API арқылы жұмыс істеу
- 🔄 Kotlin Coroutines арқылы асинхронды сұраныстар

🛠️ Қолданылған технологиялар

- Kotlin
- Android SDK
- AndroidX
- Material Components
- Retrofit
- OkHttp
- Gson
- Kotlin Coroutines
- Room Database
- Glide
- ViewModel
- Navigation Component

🏗️ Жоба құрылымы

LooksJson/
├── .gitignore
├── README.md
├── build.gradle
├── gradle.properties
├── gradlew
├── gradlew.bat
├── local.properties
├── proguard-rules.pro
├── settings.gradle
│
├── gradle/
│   └── wrapper/
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
│
└── src/
    ├── main/
    │   ├── AndroidManifest.xml
    │   │
    │   ├── java/
    │   │   └── com/
    │   │       └── afffundavbles/
    │   │           └── loockjson/
    │   │               ├── Const.kt
    │   │               ├── MainActivity.kt
    │   │               ├── SaveShared.kt
    │   │               │
    │   │               ├── data/
    │   │               │   ├── retrofit/
    │   │               │   │   ├── RetrofitRepository.kt
    │   │               │   │   └── api/
    │   │               │   │       ├── ApiService.kt
    │   │               │   │       └── RetrofitInstance.kt
    │   │               │   │
    │   │               │   └── room/
    │   │               │       ├── MoviesRoomDatabase.kt
    │   │               │       ├── dao/
    │   │               │       │   └── MoviesDao.kt
    │   │               │       └── repository/
    │   │               │           ├── MoviesRepository.kt
    │   │               │           └── MoviesRepositoryRealization.kt
    │   │               │
    │   │               ├── models/
    │   │               │   ├── MovieItemModel.kt
    │   │               │   └── MoviesModel.kt
    │   │               │
    │   │               └── screens/
    │   │                   ├── detail/
    │   │                   │   ├── DetailFragment.kt
    │   │                   │   └── DetailViewModel.kt
    │   │                   │
    │   │                   ├── favorite/
    │   │                   │   ├── FavoriteAdapter.kt
    │   │                   │   ├── FavoriteFragment.kt
    │   │                   │   └── FavoriteFragmentViewModel.kt
    │   │                   │
    │   │                   └── main/
    │   │                       ├── MainAdapter.kt
    │   │                       ├── MainFragment.kt
    │   │                       └── MainFragmentViewModel.kt
    │   │
    │   └── res/
    │       ├── drawable/
    │       │   ├── ic_baseline_favorite_24.xml
    │       │   ├── ic_baseline_favorite_border_24.xml
    │       │   └── ic_launcher_background.xml
    │       │
    │       ├── drawable-v24/
    │       │   └── ic_launcher_foreground.xml
    │       │
    │       ├── layout/
    │       │   ├── activity_main.xml
    │       │   ├── fragment_detail.xml
    │       │   ├── fragment_favorite.xml
    │       │   ├── fragment_main.xml
    │       │   └── item_layout.xml
    │       │
    │       ├── menu/
    │       │   └── main_menu.xml
    │       │
    │       ├── navigation/
    │       │   └── nav_graph.xml
    │       │
    │       ├── mipmap-anydpi-v26/
    │       │   ├── ic_launcher.xml
    │       │   └── ic_launcher_round.xml
    │       │
    │       ├── mipmap-hdpi/
    │       │   ├── ic_launcher.webp
    │       │   └── ic_launcher_round.webp
    │       │
    │       ├── mipmap-mdpi/
    │       │   ├── ic_launcher.webp
    │       │   └── ic_launcher_round.webp
    │       │
    │       ├── mipmap-xhdpi/
    │       │   ├── ic_launcher.webp
    │       │   └── ic_launcher_round.webp
    │       │
    │       ├── mipmap-xxhdpi/
    │       │   ├── ic_launcher.webp
    │       │   └── ic_launcher_round.webp
    │       │
    │       ├── mipmap-xxxhdpi/
    │       │   ├── ic_launcher.webp
    │       │   └── ic_launcher_round.webp
    │       │
    │       ├── values/
    │       │   ├── colors.xml
    │       │   ├── strings.xml
    │       │   └── themes.xml
    │       │
    │       └── values-night/
    │           └── themes.xml
    │
    ├── androidTest/
    │   └── java/
    │       └── com/
    │           └── afffundavbles/
    │               └── loockjson/
    │                   └── ExampleInstrumentedTest.kt
    │
    └── test/
        └── java/
            └── com/
                └── afffundavbles/
                    └── loockjson/
                        └── ExampleUnitTest.kt
                        ```text

🖥️ Экрандар

Негізгі экран

TMDB API арқылы алынған танымал фильмдердің тізімін көрсетеді.

Фильм экраны

Фильм туралы:

- атауы;
- шығу күні;
- сипаттамасы;
- постері;
- таңдаулыларға қосу мүмкіндігі көрсетіледі.

Таңдаулылар

Пайдаланушы таңдаулыларға қосқан фильмдер осы бөлімде сақталады.

🌐 TMDB API

Қосымша фильмдер туралы ақпарат алу үшін The Movie Database (TMDB) API қолданады.

Негізгі URL:

https://api.themoviedb.org/

Қолданылатын endpoint:

GET /3/movie/popular

Қосымшаны пайдалану үшін TMDB API кілті қажет.

«⚠️ Қазіргі нұсқада API кілті бастапқы кодтың ішінде орналасқан. Production нұсқасында API кілтін "local.properties", "BuildConfig" немесе басқа қауіпсіз конфигурацияға шығарып, оны Git репозиторийіне жарияламаған дұрыс.»

💾 Жергілікті база

Таңдаулы фильмдерді сақтау үшін Room Database қолданылады.

Фильмдер жергілікті түрде сақталады.

📋 Қажеттіліктер

- Android Studio
- JDK 8+
- Android SDK
- Android 6.0 (API 23) немесе одан жоғары
- TMDB API Key

🚀 Жобаны іске қосу

Репозиторийді жүктеп алыңыз:

git clone https://github.com/Nrskh/LooksJson.git

Содан кейін жобаны Android Studio арқылы ашып, TMDB API кілтін конфигурацияға қосыңыз.

Gradle синхрондалғаннан кейін қосымшаны эмуляторда немесе Android құрылғысында іске қосуға болады.

🧪 Тестілеу

Жобада:

- Unit-тесттер;
- Instrumented-тесттер бар.

Тесттерді іске қосу:

./gradlew test

Windows үшін:

gradlew.bat test

📄 Лицензия

Қазіргі уақытта жобада жеке лицензия көрсетілмеген.

---

🇬🇧 English

📱 About

LoockJson is an Android application built with Kotlin that uses the The Movie Database (TMDB) API to retrieve information about popular movies.

Users can browse popular movies, open a movie details page, and save movies to their favorites.

✨ Features

- 🎬 Fetch popular movies from TMDB
- 🖼️ Display movie posters
- 📄 View movie details:
  - title
  - release date
  - overview
  - poster
- ❤️ Add and remove movies from favorites
- 💾 Store favorite movies locally
- 🌐 REST API integration
- 🔄 Asynchronous API requests using Kotlin Coroutines

🛠️ Technologies

- Kotlin
- Android SDK
- AndroidX
- Material Components
- Retrofit
- OkHttp
- Gson
- Kotlin Coroutines
- Room Database
- Glide
- ViewModel
- Navigation Component

🏗️ Project Structure

LooksJson/
├── .gitignore
├── README.md
├── build.gradle
├── gradle.properties
├── gradlew
├── gradlew.bat
├── local.properties
├── proguard-rules.pro
├── settings.gradle
│
├── gradle/
│   └── wrapper/
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
│
└── src/
    ├── main/
    │   ├── AndroidManifest.xml
    │   │
    │   ├── java/
    │   │   └── com/
    │   │       └── afffundavbles/
    │   │           └── loockjson/
    │   │               ├── Const.kt
    │   │               ├── MainActivity.kt
    │   │               ├── SaveShared.kt
    │   │               │
    │   │               ├── data/
    │   │               │   ├── retrofit/
    │   │               │   │   ├── RetrofitRepository.kt
    │   │               │   │   └── api/
    │   │               │   │       ├── ApiService.kt
    │   │               │   │       └── RetrofitInstance.kt
    │   │               │   │
    │   │               │   └── room/
    │   │               │       ├── MoviesRoomDatabase.kt
    │   │               │       ├── dao/
    │   │               │       │   └── MoviesDao.kt
    │   │               │       └── repository/
    │   │               │           ├── MoviesRepository.kt
    │   │               │           └── MoviesRepositoryRealization.kt
    │   │               │
    │   │               ├── models/
    │   │               │   ├── MovieItemModel.kt
    │   │               │   └── MoviesModel.kt
    │   │               │
    │   │               └── screens/
    │   │                   ├── detail/
    │   │                   │   ├── DetailFragment.kt
    │   │                   │   └── DetailViewModel.kt
    │   │                   │
    │   │                   ├── favorite/
    │   │                   │   ├── FavoriteAdapter.kt
    │   │                   │   ├── FavoriteFragment.kt
    │   │                   │   └── FavoriteFragmentViewModel.kt
    │   │                   │
    │   │                   └── main/
    │   │                       ├── MainAdapter.kt
    │   │                       ├── MainFragment.kt
    │   │                       └── MainFragmentViewModel.kt
    │   │
    │   └── res/
    │       ├── drawable/
    │       │   ├── ic_baseline_favorite_24.xml
    │       │   ├── ic_baseline_favorite_border_24.xml
    │       │   └── ic_launcher_background.xml
    │       │
    │       ├── drawable-v24/
    │       │   └── ic_launcher_foreground.xml
    │       │
    │       ├── layout/
    │       │   ├── activity_main.xml
    │       │   ├── fragment_detail.xml
    │       │   ├── fragment_favorite.xml
    │       │   ├── fragment_main.xml
    │       │   └── item_layout.xml
    │       │
    │       ├── menu/
    │       │   └── main_menu.xml
    │       │
    │       ├── navigation/
    │       │   └── nav_graph.xml
    │       │
    │       ├── mipmap-anydpi-v26/
    │       │   ├── ic_launcher.xml
    │       │   └── ic_launcher_round.xml
    │       │
    │       ├── mipmap-hdpi/
    │       │   ├── ic_launcher.webp
    │       │   └── ic_launcher_round.webp
    │       │
    │       ├── mipmap-mdpi/
    │       │   ├── ic_launcher.webp
    │       │   └── ic_launcher_round.webp
    │       │
    │       ├── mipmap-xhdpi/
    │       │   ├── ic_launcher.webp
    │       │   └── ic_launcher_round.webp
    │       │
    │       ├── mipmap-xxhdpi/
    │       │   ├── ic_launcher.webp
    │       │   └── ic_launcher_round.webp
    │       │
    │       ├── mipmap-xxxhdpi/
    │       │   ├── ic_launcher.webp
    │       │   └── ic_launcher_round.webp
    │       │
    │       ├── values/
    │       │   ├── colors.xml
    │       │   ├── strings.xml
    │       │   └── themes.xml
    │       │
    │       └── values-night/
    │           └── themes.xml
    │
    ├── androidTest/
    │   └── java/
    │       └── com/
    │           └── afffundavbles/
    │               └── loockjson/
    │                   └── ExampleInstrumentedTest.kt
    │
    └── test/
        └── java/
            └── com/
                └── afffundavbles/
                    └── loockjson/
                        └── ExampleUnitTest.kt
                        ```text

🖥️ Screens

Main Screen

Displays a list of popular movies retrieved from the TMDB API.

Movie Details

Displays:

- movie title;
- release date;
- overview;
- poster;
- favorite button.

Favorites

Displays movies saved by the user locally.

🌐 TMDB API

The application uses The Movie Database (TMDB) API to retrieve movie information.

Base URL:

https://api.themoviedb.org/

Endpoint:

GET /3/movie/popular

A TMDB API key is required to use the application.

«⚠️ The current version contains the API key directly in the source code. For production, it is recommended to move the key to "local.properties", "BuildConfig", or another secure configuration method and keep it out of Git.»

💾 Local Storage

Room Database is used to store favorite movies locally.

This allows favorite movies to remain available after restarting the application.

📋 Requirements

- Android Studio
- JDK 8+
- Android SDK
- Android 6.0 (API 23) or higher
- TMDB API Key

🚀 Getting Started

Clone the repository:

git clone https://github.com/Nrskh/LooksJson.git

Open the project in Android Studio, configure your TMDB API key, sync Gradle, and run the application on an emulator or Android device.

🧪 Testing

The project contains:

- Unit tests
- Instrumented tests

Run unit tests:

./gradlew test

On Windows:

gradlew.bat test

📄 License

No separate license has been specified for the project yet.

---

👨‍💻 Author

Nrskh

GitHub:
https://github.com/Nrskh

---

⭐ Support

If you find the project useful, consider giving the repository a ⭐.
