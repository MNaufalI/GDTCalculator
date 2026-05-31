# GDT Calculator

A companion app for **Game Dev Tycoon** that helps players make optimal decisions when developing games.

---

## Features

- **Topic Search** — Browse all topics with genre and audience ratings. Selecting a topic auto-highlights the best matching genres.
- **Smart Filter** — Table filters dynamically as you select genres and audience, showing only `+++` and `++` rated topics.
- **Platform Suggestion** — Get platform recommendations based on your selected genre and audience combination.
- **Development Guide** — View slider focus and Tech/Design balance for each development phase.
- **Bookmark System** — Save favorite topic + genre combinations and load them instantly.

## Tech Stack

- **Language:** Kotlin
- **UI:** Jetpack Compose
- **Architecture:** MVVM
- **Navigation:** Navigation Compose
- **Storage:** DataStore + Kotlin Serialization (JSON)

## Project Structure

```
app/
└── src/main/java/com/naufal/gdtcalculator/
    ├── data/
    │   ├── model/        — Data classes + interfaces (RatingMatrix, DevData)
    │   └── repository/   — GDTRepository, BookmarkRepository
    ├── ui/
    │   ├── base/         — BaseViewModel, Interfaces, HighlightHelper
    │   ├── topic/        — Topic selection with auto-genre detection
    │   ├── review/       — Summary + bookmark toggle
    │   ├── platform/     — Platform suggestion
    │   ├── development/  — Dev phase slider guide
    │   └── bookmark/     — Saved combinations
    └── navigation/       — AppNavigation + Screen routes
```

## How to Use

1. Tap **Topic** from the home screen
2. Select a topic from the table — genres will auto-highlight based on `+++` ratings
3. Adjust genre and audience if needed
4. Tap **OK → View Review** to see your combination summary
5. Proceed to **Platform Suggestion** and **Development Phases**
6. Bookmark your favorite combinations for quick access later

## Build

```bash
# Clone the repository
git clone https://github.com/MNaufalI/GDTCalculator.git

# Open in Android Studio and run
# Min SDK: check build.gradle.kts
```

---

*Based on data from Game Dev Tycoon by Greenheart Games.*

Contributor:
Muhammad Naufal Idzhaarulhaq aka Karbit
Muhammad Fauzan Habibi aka Foxsix
