# 🧭 Tour Guide

### Pick Places. Build Your Trail. Walk Bengaluru.

Tour Guide is an Android application developed using **Kotlin and XML layouts**. It provides users with a simple and attractive interface to plan a heritage walk through central Bengaluru by choosing landmarks, building a trail, and viewing the walking route on Google Maps.

The application features a landmark list with category filters, a trail builder with distance and walking-time estimates, and an in-app Google Map displayed using WebView.

---

## 📱 Screenshots

### 1. Home Screen

The home screen shows the app header, category filters, the map of central Bengaluru, and the list of landmarks to choose from.

![Tour Guide Home Screen](screenshots/home-screen.png)

### 2. Building a Trail

Tapping **Add** on a place makes it the next stop. Each card shows its stop number and the distance from the previous stop.

![Tour Guide Building a Trail](screenshots/building-a-trail.png)

### 3. Walking Route

With two or more stops, the map shows Google Maps walking directions through every stop, with the total distance and walking time above it.

![Tour Guide Walking Route](screenshots/walking-route.png)

---

## ✨ Features

- **Landmark List:** 12 well-known places in central Bengaluru, each with a short description.
- **Category Filters:** Filter places by Heritage, Parks, Food, or Culture. Places already on the trail always stay visible.
- **Trail Builder:** Add or remove stops with one tap. Each card shows its stop number and the distance from the previous stop.
- **Walking Route:** Google Maps walking directions through all stops, in order.
- **Trail Summary:** Number of stops, total distance, and estimated walking time at 4.8 km/h.
- **Place Focus:** Tap a card to see that place on the map.
- **Map Controls:** Switch between Map, Satellite, and Terrain views, fit the whole trail on screen, or open the current place or route in the Google Maps app.
- **In-App WebView Map:** Google's embeddable map is displayed inside the app, with no API key required.
- **Loading Indicator:** A progress bar is shown while the map loads.
- **Error Handling:** A message with a **Retry** button appears if the map cannot load.
- **State Restoration:** The trail, selected place, filter, and map type are kept when the screen rotates.
- **Simple User Interface:** A cream-and-green color palette for a clean appearance.

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Kotlin | Application programming logic |
| XML | Designing application layouts |
| Android Studio | Application development environment |
| Android WebView | Displaying the Google Map inside the app |
| Material Components | Chips, buttons, floating action buttons, and progress indicator |
| JUnit 4 | Unit testing of distance and URL logic |
| Gradle (Kotlin DSL) | Project build and dependency management |
| Android SDK | Android application development (min SDK 26, target SDK 37) |

---

## 📂 Project Structure

```text
TourGuide/
│
├── app/
│   ├── build.gradle.kts
│   └── src/
│       ├── main/
│       │   ├── java/
│       │   │   └── com/
│       │   │       └── rohit/
│       │   │           └── tourguide/
│       │   │               ├── MainActivity.kt
│       │   │               └── Trail.kt
│       │   │
│       │   ├── res/
│       │   │   ├── layout/
│       │   │   │   ├── activity_main.xml
│       │   │   │   ├── row_place.xml
│       │   │   │   └── chip_filter.xml
│       │   │   │
│       │   │   ├── drawable/
│       │   │   ├── color/
│       │   │   ├── xml/
│       │   │   └── values/
│       │   │       ├── strings.xml
│       │   │       └── themes.xml
│       │   │
│       │   └── AndroidManifest.xml
│       │
│       └── test/
│           └── java/
│               └── com/
│                   └── rohit/
│                       └── tourguide/
│                           └── TrailMathTest.kt
│
├── gradle/
│   └── libs.versions.toml
│
├── screenshots/
│   ├── home-screen.png
│   ├── building-a-trail.png
│   └── walking-route.png
│
├── README.md
├── build.gradle.kts
└── settings.gradle.kts
```

*Note: `MainActivity.kt` handles the screen and map, while `Trail.kt` holds the places, distance calculations, and Google Maps URLs. Gradle wrapper files and some resource files are omitted for brevity.*

---

## ⚙️ Installation and Setup

Follow these steps to run Tour Guide on your computer.

### Prerequisites

- Android Studio installed on your computer.
- Android SDK Platform 37 configured.
- An Android emulator or a physical Android device (Android 8.0 or higher).
- An active internet connection.

### Steps to Run

1. Clone or download this repository from GitHub.
2. Open Android Studio.
3. Select **Open** and choose the TourGuide project folder.
4. Wait for Gradle synchronization to complete.
5. Start an Android emulator or connect a physical Android device.
6. Click the **Run ▶** button.
7. Wait for the application to install and launch.

You can now explore the Tour Guide landmarks and build your own trail.

### Run the Unit Tests

```bash
./gradlew test        # macOS / Linux
gradlew.bat test      # Windows
```

---

## 🌐 Internet Permission

Tour Guide uses Android WebView to display Google Maps inside the application.

The application requires internet permission in `AndroidManifest.xml`.

```xml
<uses-permission android:name="android.permission.INTERNET" />
```

This permission should be declared outside the `<application>` element.

An active internet connection is required to load the map. The map uses Google's embeddable web map, so no Google Maps API key is needed.

---

## 🧭 Application Controls

The application provides the following controls:

| Control | Description |
|---|---|
| Category Chips | Filter the list by All, Heritage, Parks, Food, or Culture |
| Place Card | Shows that place on the map |
| Add / Added Button | Adds the place to the trail or removes it |
| Clear | Removes all stops from the trail |
| Layers Button | Switches between Map, Satellite, and Terrain views |
| Fit Button | Shows the whole trail on the map |
| Open Button | Opens the current place or route in the Google Maps app or browser |
| Retry | Reloads the map after a connection problem |

The map is displayed within the application using Android WebView.

---

## 🎯 Project Objective

The main objective of Tour Guide is to develop a simple Android application that helps users plan a walking tour of Bengaluru's landmarks through a user-friendly interface.

This project also demonstrates fundamental Android development concepts, including:

- Activity creation and lifecycle handling.
- XML-based user interface design.
- Kotlin programming.
- Android WebView integration with Google Maps.
- Internet permission handling.
- Saving and restoring state on screen rotation.
- Opening other apps using intents.
- Distance calculation using the haversine formula.
- Unit testing with JUnit.

---

## 🚀 Future Enhancements

The following improvements can be added in future versions:

- Save trails so they are kept after the app is closed.
- Add a search feature for places.
- Show the user's current location on the map.
- Add photos and detailed descriptions for each place.
- Show real walking distance and time from a routing API.
- Add more places and other cities.
- Let users add their own custom places.
- Share a trail with friends.
- Add a dark theme.
- Improve accessibility and responsive layouts.

---

## 📚 Learning Outcomes

Developing Tour Guide provides practical experience with:

1. Building Android applications using Kotlin.
2. Designing layouts using XML and Material Components.
3. Integrating WebView with an embedded Google Map.
4. Managing internet permissions.
5. Handling configuration changes and saved instance state.
6. Using intents to open external apps.
7. Writing unit tests for application logic.
8. Organizing an Android Studio project.

---

## 👨‍💻 Author

**Rohit Kumar Singh**

MCA Student | Aspiring Software Developer

---
