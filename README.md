# Shree Hari Om App

Shree Hari Om App is an Android application for **Shree Hari Om Enterprises**, providing an interface for AC servicing, repairs, installation, rental and purchase options, AMC plans, sell/exchange inquiries, and invoice or quotation generation.

The app uses an Android `WebView` to display the complete user interface from `app/src/main/assets/index.html`.

## Features

- AC service search and booking
- Jet servicing, gas refills, repairs, and installation/uninstallation
- New and refurbished AC buy/rent listings
- Old AC sell/exchange inquiries
- Annual Maintenance Contract (AMC) plans
- Pre-service quotations and post-service invoices
- GST and document print/PDF support
- Mobile and desktop-style responsive previews
- Direct-call and in-app navigation support

## Technology Stack

- **Platform:** Android
- **Language:** Kotlin
- **UI:** HTML, Tailwind CSS, and JavaScript
- **Android components:** WebView, AppCompat
- **Build system:** Gradle Kotlin DSL
- **Android SDK:** Compile SDK 34
- **Minimum Android:** API 24 (Android 7.0)
- **Java compatibility:** Java 17

## Project Structure

```text
.
├── app/
│   ├── build.gradle.kts
│   └── src/main/
│       ├── AndroidManifest.xml
│       ├── assets/
│       │   └── index.html
│       └── kotlin/org/example/
│           └── MainActivity.kt
├── build.gradle.kts
├── settings.gradle.kts
└── gradle.properties
```

- `MainActivity.kt` creates the Android WebView and loads the bundled HTML interface.
- `index.html` contains the application layout, mock data, navigation, forms, and document-generation logic.
- `AndroidManifest.xml` declares application permissions and the launcher activity.

## Requirements

- Android Studio with an Android SDK
- Android SDK Platform 34
- JDK 17
- An Android emulator or physical device running Android 7.0 (API 24) or newer

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/shelkesachin2907/ShreeHariOmApp.git
cd ShreeHariOmApp
```

### 2. Open in Android Studio

Open the project directory in Android Studio and allow Gradle to synchronize dependencies.

### 3. Run the app

Select an emulator or connected Android device, then run:

```bash
./gradlew assembleDebug
```

The debug APK will be generated at:

```text
app/build/outputs/apk/debug/app-debug.apk
```

You can also install and launch the app from Android Studio using the **Run** action.

## Build a Release APK

```bash
./gradlew assembleRelease
```

The unsigned release APK will be generated under:

```text
app/build/outputs/apk/release/
```

## Application Configuration

- **Package name:** `org.example.shreehariom`
- **Namespace:** `org.example`
- **Version:** `1.0` (`versionCode 1`)
- **Target SDK:** 34
- **Minimum SDK:** 24

Update these values in `app/build.gradle.kts` when preparing the app for publication.

## Permissions

The app declares the following permissions:

- Internet access
- Network state access
- Phone calling

The telephony feature is optional and is marked with `android:required="false"` so the app can also run on non-phone devices.

## Current Status

This project is a functional frontend prototype. Service bookings, sales inquiries, and generated documents currently use local browser logic and alert confirmations; they do not yet save data to a backend or send messages to an external server.

Before production use, add:

- Backend/API integration
- Persistent customer and document storage
- Authentication for staff and customers
- Real payment processing
- Server-side GST and invoice validation
- Input validation and secure handling of customer data
- Confirmation notifications by SMS, WhatsApp, or email

## Contributing

Contributions are welcome.

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push the branch
5. Open a pull request

## License

No license is currently specified. All rights may remain with the repository owner until a license is added.
