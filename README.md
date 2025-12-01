# Hey there! I'm Alfonso 

Computer Science graduate and passionate of new technologies. <br/>
iOS Engineer focused on scalable architectures, clean code and high-quality user experiences. I’ve spent the last years building large-scale iOS apps at Nomasystems for Inditex (Zara Home and other core apps), using Clean Architecture, MVVM + Coordinators, SwiftUI and Swift Concurrency, as well as legacy UIKit code <br/>
I enjoy owning modules end-to-end: from collaborating with design and product, to defining the architecture, implementing features, writing tests and improving performance. <br/>
 I’m especially interested in applying new Apple technologies (SwiftData, SwiftUI) and AI to real products and to my daily workflow.

# Personal projects

## [Renn - Running app](https://github.com/bzas/Running-app-ios) (Work in Progress)

iOS application (SwiftUI) for running data and stats.

### Architecture

The app follows a modular Clean Architecture combined with MVVM and a Coordinator system to ensure scalability, testability, and maintainability. Each layer has a clear responsibility and communicates only through well-defined interfaces.

<img src="https://github.com/bzas/bzas/blob/main/images/Renn/Architecture.svg" width="600" />

The project is divided into independent modules:
- App:
    - Main app target, AppCoordinator, AppAssembly and DependencyContainer
    - It's main responsability is the creation and wiring of Coordinators, ViewModels, and global services
    - It consumes UseCases provided by the Application layer and injects them into the UI
- Domain:
    - Domain entities and repository protocols used by UseCases
    - This layer has no dependency on UI, database, or frameworks
- Application:
    - Contains the UseCase definition and their dependencies
    - This layer defines application-level actions (e.g. importing a FIT file, loading workouts, managing the user)
    - It knows what operations the app performs but doesn’t contain UI code
- Database:
    - Data models and mappers
    - Repository implementations (conforming to domain protocols)
    - Local persistence (SwiftData)
    - This layer transforms external data into Domain models
- GarminKit:
    - Handles parsing and mapping of Garmin .fit files into Database models
    - Based on FITSwiftSDK
    - Garmin DTO models
- Features: (Workouts, Profile, Launch, Search, WorkoutDetail)
    - Its own Coordinator
    - A RootView
    - An Assembly protocol
    - Local ViewModels
    - Features remain isolated and only depend on Domain + their UseCases.
- Localization: String localizations
- Common: Reusable components, entities....etc

### Features

<p align="left">
<img src="https://github.com/bzas/bzas/blob/main/images/Renn/Detail.PNG" width="275" />
<img src="https://github.com/bzas/bzas/blob/main/images/Renn/Profile.PNG" width="275" />
<img src="https://github.com/bzas/bzas/blob/main/images/Renn/HeartRate.PNG" width="275" />
<img src="https://github.com/bzas/bzas/blob/main/images/Renn/DetailInfo.PNG" width="275" />
<img src="https://github.com/bzas/bzas/blob/main/images/Renn/Metrics.PNG" width="275" />
<img src="https://github.com/bzas/bzas/blob/main/images/Renn/Workouts.PNG" width="275" />
</p>

- Garmin integration for reading fitness data
- Route mapping (MapKit) and real-time route tracking
- Workout history and session details
- Graphs (pace, heart rate, elevation, heart rate zones...etc)
- Goals, personal records, stats


## [Showtime Hub - Movies & Series](https://github.com/bzas/Showtime-Hub)

The definitive application for all lovers of movies and TV series. With Showtime Hub, keeping track of your favorite movies and series has never been easier and more fun. Designed to be intuitive and elegant, our app allows you to manage all your audiovisual content in an efficient and personalized way.
- Create and organize your personal library of movies and series.
- Easily add titles with our advanced search feature
- Mark the movies and series you have already seen.
- Maintain an up-to-date list of pending titles to watch.
- Customize the UI

<p float="left">
  <img src="https://github.com/bzas/bzas/blob/main/images/ShowTimeHub/capture-1.png" width="275" />
  <img src="https://github.com/bzas/bzas/blob/main/images/ShowTimeHub/capture-2.png" width="275" />
  <img src="https://github.com/bzas/bzas/blob/main/images/ShowTimeHub/capture-3.png" width="275" />
</p>

# My tech stack

##### Plattforms <br/>
<img src="https://img.shields.io/badge/iOS-3b3939?style=for-the-badge&logo=apple&logoColor=ffffff" /> <img src="https://img.shields.io/badge/macos-ffffff?style=for-the-badge&logo=macos&logoColor=000" /> <img src="https://img.shields.io/badge/App_Store_Publishing-ffffff?style=for-the-badge&logo=app%20store" /> <br/>

##### Languages and Frameworks <br/>
<img src="https://img.shields.io/badge/Swift-f72d00?style=for-the-badge&logo=Swift&logoColor=FFFFFF" /> <img src="https://img.shields.io/badge/objective%20c-706d6d?style=for-the-badge&logo=objective-c&logoColor=FFFFFF" /> <br/>
<img src="https://img.shields.io/badge/uikit-3ba4f5?style=for-the-badge&logo=uikit&logoColor=ffffff" /> <img src="https://img.shields.io/badge/swiftui-f5823b?style=for-the-badge&logo=swift&logoColor=ffffff" /> <br/>

##### Developer tools <br/>
<img src="https://img.shields.io/badge/Xcode-2e75b3?style=for-the-badge&logo=Xcode&logoColor=FFFFFF" /> <img src="https://img.shields.io/badge/Visual%20studio%20code-14bdfa?style=for-the-badge&logo=visual%20studio%20code&logoColor=ffffff" /> <br/> 
<img src="https://img.shields.io/badge/swiftlint-ce2ad4?style=for-the-badge&logo=swift&logoColor=ffffff" />
<img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=Postman&logoColor=white" />
<br/>

##### Source Control & CI/CD
<img src="https://img.shields.io/badge/git-ff0000?style=for-the-badge&logo=git&logoColor=ffffff" /> <img src="https://img.shields.io/badge/github-8400ff?style=for-the-badge&logo=github&logoColor=ffffff" /> <br/>
<img src="https://img.shields.io/badge/github%20actions-367d2e?style=for-the-badge&logo=GitHub%20actions&logoColor=ffffff" /> <img src="https://img.shields.io/badge/fastlane-85fc49?style=for-the-badge&logo=fastlane&logoColor=000" />

##### Other tools
<img src="https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=Jira&logoColor=white" /> <img src="https://img.shields.io/badge/Confluence-0052CC?style=for-the-badge&logo=Confluence&logoColor=FFFFFF" /> <br/>
<img src="https://img.shields.io/badge/Firebase-3993fa?style=for-the-badge&logo=firebase" /> <img src="https://img.shields.io/badge/figma-82faa6?style=for-the-badge&logo=figma&logoColor=000" />  <img src="https://img.shields.io/badge/chat%20gpt-8acfb0?style=for-the-badge&logo=openai&logoColor=000000" />

# Contact me

<a href="https://www.linkedin.com/in/alfonso-boizas/"> <img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /> </a>
<a href="mailto:boizasal@gmail.com"> <img src="https://img.shields.io/badge/boizasal@gmail.com-%23D14836.svg?&style=for-the-badge&logo=gmail&logoColor=white" /> </a>

  ![Profile views](https://komarev.com/ghpvc/?username=bzas&label=Profile%20views&color=0e75b6&style=flat)

