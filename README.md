
##  𝐆𝐞𝐦𝐢𝐧𝐢 𝐂𝐡𝐚𝐭 𝐀𝐩𝐩

**Gemini Android** demonstrates [Google's Generative AI](https://android-developers.googleblog.com/2023/12/leverage-generative-ai-in-your-android-apps.html) on Android with [Stream Chat SDK for Compose](https://getstream.io/tutorials/android-chat?utm_source=Github&utm_medium=Github_Repo_Content_Ad&utm_content=Developer&utm_campaign=Github_Dec2024_Jaewoong_Gemini&utm_term=DevRelOss).

<p align="center">
  <a href="https://opensource.org/licenses/Apache-2.0"><img alt="License" src="https://img.shields.io/badge/License-Apache%202.0-blue.svg"/></a>
  <a href="https://android-arsenal.com/api?level=21"><img alt="API" src="https://img.shields.io/badge/API-21%2B-brightgreen.svg?style=flat"/></a>
  <a href="https://github.com/skydoves/gemini-android/actions/workflows/android.yml"><img alt="Build Status" src="https://github.com/skydoves/gemini-android/actions/workflows/android.yml/badge.svg"/></a>
</p>

The purpose of this repository is to demonstrate below:

- Demonstrates [Gemini API](https://ai.google.dev/tutorials/android_quickstart) for Android.
- Implementing entire UI elements with Jetpack Compose.
- Implementation of Android architecture components with Jetpack libraries such as Hilt and AppStartup.
- Performing background tasks with Kotlin Coroutines.
- Integrating chat systems with [Stream Chat Compose SDK](https://getstream.io/tutorials/android-chat?utm_source=Github&utm_medium=Github_Repo_Content_Ad&utm_content=Developer&utm_campaign=Github_Dec2024_Jaewoong_Gemini&utm_term=DevRelOss) for real-time event handling.

## 📷 Previews

<p align="center">
<img src="previews/preview0.png" alt="drawing" width="270px" />
<img src="previews/preview1.png" alt="drawing" width="270px" />
<img src="previews/preview2.gif" alt="drawing" width="269px" /></br>
</p>

## 🛠 Tech Stack & Open Source Libraries
- Minimum SDK level 21.
- 100% [Jetpack Compose](https://developer.android.com/jetpack/compose) based + [Coroutines](https://github.com/Kotlin/kotlinx.coroutines) + [Flow](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/) for asynchronous.
- [Compose Chat SDK for Messaging](https://getstream.io/chat/sdk/compose?utm_source=Github?utm_source=Github&utm_medium=Github_Repo_Content_Ad&utm_content=Developer&utm_campaign=Github_Dec2024_Jaewoong_Gemini&utm_term=DevRelOss): The Jetpack Compose Chat Messaging SDK is built on a low-level chat client and provides modular, customizable Compose UI components that you can easily drop into your app.
- Jetpack
  - Compose: Android’s modern toolkit for building native UI.
  - ViewModel: UI related data holder and lifecycle aware.
  - App Startup: Provides a straightforward, performant way to initialize components at application startup.
  - Navigation: For navigating screens and [Hilt Navigation Compose](https://developer.android.com/jetpack/compose/libraries#hilt) for injecting dependencies.
  - Room: Constructs Database by providing an abstraction layer over SQLite to allow fluent database access.
  - Datastore: Store data asynchronously, consistently, and transactionally, overcoming some of the drawbacks of SharedPreferences.
  - [Hilt](https://dagger.dev/hilt/): Dependency Injection.
- [Landscapist Glide](https://github.com/skydoves/landscapist#glide), [animation](https://github.com/skydoves/landscapist#animation), [placeholder](https://github.com/skydoves/landscapist#placeholder): Jetpack Compose image loading library that fetches and displays network images with Glide, Coil, and Fresco.
- [Retrofit2 & OkHttp3](https://github.com/square/retrofit): Construct the REST APIs and paging network data.
- [Sandwich](https://github.com/skydoves/Sandwich): Construct a lightweight and modern response interface to handle network payload for Android.
- [Moshi](https://github.com/square/moshi/): A modern JSON library for Kotlin and Java.
- [ksp](https://github.com/google/ksp): Kotlin Symbol Processing API.
- [Balloon](https://github.com/skydoves/balloon): Modernized and sophisticated tooltips, fully customizable with an arrow and animations for Android.
- [StreamLog](https://github.com/GetStream/stream-log): A lightweight and extensible logger library for Kotlin and Android.
- Baseline Profiles: To improve app performance by including a list of classes and methods specifications in your APK that can be used by Android Runtime.

## 🏛️ Architecture

**Gemini Android** follows the [Google's official architecture guidance](https://developer.android.com/topic/architecture).

![architecture](figures/figure0.png)

**Gemini Android** was built with [Guide to app architecture](https://developer.android.com/topic/architecture), so it would be a great sample to show how the architecture works in real-world projects.<br>

The overall architecture is composed of two layers; UI Layer and the data layer. Each layer has dedicated components and they each have different responsibilities.
The arrow means the component has a dependency on the target component following its direction.

### Architecture Overview

![layer](figures/figure1.png)

Each layer has different responsibilities below. Basically, they follow [unidirectional event/data flow](https://developer.android.com/topic/architecture/ui-layer#udf).

### UI Layer

![layer](figures/figure2.png)

The UI Layer consists of UI elements like buttons, menus, tabs that could interact with users and [ViewModel](https://developer.android.com/topic/libraries/architecture/viewmodel) that holds app states and restores data when configuration changes.

### Data Layer

![layer](figures/figure3.png)

The data Layer consists of repositories, which include business logic, such as querying data from the local database and requesting remote data from the network. It is implemented as an offline-first source of business logic and follows the [single source of truth](https://en.wikipedia.org/wiki/Single_source_of_truth) principle.<br>

For more information about the overall architecture, check out **[Build a Real-Time WhatsApp Clone With Jetpack Compose](https://getstream.io/blog/build-whatsapp-clone/)**.

## Modularization

![02](https://github.com/skydoves/gemini-android/assets/24237865/7b0cc635-83b0-434c-b151-d0e0e0a2ff9b)

**Gemini Android** has implemented the following modularization strategies:

- **Reusability**: By effectively modularizing reusable code, it not only facilitates code sharing but also restricts code access across different modules.

- **Parallel Building**: Modules are capable of being built in parallel, leading to reduced overall build time.

- **Decentralized Focusing**: Individual development teams are allocated specific modules, allowing them to concentrate on their designated areas.


## 💯 MAD Score

![summary](https://user-images.githubusercontent.com/24237865/158918011-bc766482-ec83-47dd-9237-d8a226cab263.png)


