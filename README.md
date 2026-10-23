# MECHZO AOU GRADUATION PROJECT

## Project Overview

**MECHZO** is the graduation project completed as part of the **Arab Open University (AOU)** degree program. The project demonstrates a full‑cycle software development workflow using modern build tools and a modular codebase. It showcases the ability to design, implement, and deliver a complete application from concept to deployment, adhering to industry best practices.

## Tech Stack

- **Build System:** Gradle (configured via `settings.gradle.kts`)
- **Repositories:** Google Maven Central (declared in `settings.gradle.kts`)
- **Module Structure:** Root project includes `:app` module
- **Language:** Kotlin / Java (compatible with Gradle JVM/Kotlin DSL)
- **IDE Support:** Android Studio / IntelliJ IDEA

## Project Structure

```
MECHZO/
├── .gitignore               # excludes Gradle, IDE, local properties, etc.
├── settings.gradle.kts      # plugin management and module inclusion
├── build.gradle.kts         # root build configuration (plugins, versioning)
├── gradle/                # Gradle wrapper files
├── app/
│   ├── build.gradle.kts     # module‑specific dependencies and tasks
│   ├── src/
│     ├── main/
│     │   └── ...            # main source set (Android/java resources)
│   │   └── ...
│   ├── test/
│   │   └── ...              # unit tests
│   └── ...
├── .idea/                 # IntelliJ/Android Studio project files
├── local.properties       # local SDK/NDK paths (git‑ignored)
├── gradle.properties      # Gradle version and property tweaks
└── README.md              # this file
```

- **Root (`settings.gradle.kts`)** declares the project name (`MECHZO`), plugin repositories, and includes the `:app` module.
- **Module `:app`** contains the actual application source code, its own `build.gradle.kts`, and the standard Android source sets.

## Getting Started / Setup Instructions

1. **Clone the repository**

   ```bash
   git clone https://github.com/your‑username/MECHZO-AOU-GRADUATION-PROJECT.git
   cd MECHZO-AOU-GRADUATION-PROJECT
   ```

2. **Verify Git configuration (optional)**

   ```bash
   git config user.name "Your Name"
   git config user.email "you@example.com"
   ```

3. **Build the project**

   Using the Gradle wrapper:

   ```bash
   ./gradlew build
   ```

   This compiles the source, runs unit tests, and generates any build artifacts.

4. **Run / inspect the app (Android)**

   - Open the project in **Android Studio**: `File → Open → gradle/app/build.gradle.kts` (or just the root `build.gradle.kts`).
   - Connect an Android device or start an emulator.
   - Click **Run** (the green play button) or execute:

     ```bash
     ./gradlew installDebug
     ```

     to install the debug APK.

5. **Optional: Run tests**

   ```bash
   ./gradlew test
   ```

6. **Commit your changes (if working locally)**

   ```bash
   git add .
   git commit -m "Descriptive commit message"
   git push origin main
   ```

---

**Happy coding!** If you encounter any issues, consult the Gradle documentation or the `:app` module’s `build.gradle.kts` for dependency details.