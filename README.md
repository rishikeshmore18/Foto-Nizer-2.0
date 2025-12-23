# Foto-Nizer

Android application built with Kotlin and Jetpack Compose.

## Getting Started

### Prerequisites
- Android Studio (latest version)
- JDK 11 or higher
- Android SDK 24+

### Building the Project

```bash
# Build the project
./gradlew build

# Build release APK
./gradlew assembleRelease

# Build release AAB (for Play Store)
./gradlew bundleRelease
```

### Running the App

1. Open the project in Android Studio
2. Sync Gradle files
3. Run on an emulator or connected device

## Deployment

This project uses GitHub Actions for automated builds and releases.

### Automatic Deployment

- **Push to main/master**: Automatically builds the project and creates artifacts
- **Create a tag**: Pushing a tag starting with `v` (e.g., `v1.0.0`) automatically creates a GitHub release with APK and AAB files

### Manual Release Process

1. Update version in `app/build.gradle.kts`:
   ```kotlin
   versionCode = 2
   versionName = "1.0.1"
   ```

2. Commit and push:
   ```bash
   git add .
   git commit -m "chore: bump version to 1.0.1"
   git push origin main
   ```

3. Create and push a tag:
   ```bash
   git tag v1.0.1
   git push origin v1.0.1
   ```

4. GitHub Actions will automatically create a release with the built artifacts.

## Project Structure

```
FotoNizer/
├── app/
│   ├── build.gradle.kts
│   └── src/
├── build.gradle.kts
├── settings.gradle.kts
└── gradle/
```

## CI/CD

The project includes a GitHub Actions workflow (`.github/workflows/deploy.yml`) that:
- Builds the project on every push to main/master
- Creates APK and AAB artifacts
- Automatically creates releases when tags are pushed

## License

[Add your license here]

