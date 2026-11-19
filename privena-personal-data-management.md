# Portfolio Project Data — Privena - Personal Data Management

- **Category:** `desktop-mobile` (Mobile App)
- **Category Label:** `Mobile App`
- **Accent Color:** `amber`
- **Target Assets Folder:** `public/images/projects/privena_personal_data_management/`
- **Required Local Images:** `banner.webp`, `image01.webp`, `image02.webp`

## TypeScript Data (`ProjectCaseStudy`)

```typescript
{
  "id": "privena-personal-data-management",
  "code": "PRO-22 // APP-01",
  "title": "Privena - Personal Data Management",
  "category": "desktop-mobile",
  "categoryLabel": "Mobile App",
  "year": "2022",
  "status": "Completed",
  "accentColor": "amber",
  "repoUrl": "https://github.com/weztcy/Privena---Personal-Data-Management",
  "license": "MIT License",
  "imageUrl": "/images/projects/privena_personal_data_management/banner.webp",
  "images": [
    "/images/projects/privena_personal_data_management/banner.webp"
  ],
  "summary": "Native Android personal vault app utilizing Realm DB and Firebase to store and manage sensitive credentials offline with secure cloud authentication.",
  "projectDescription": "Privena is a native Android personal data vault built with Java and Realm DB, engineered to safeguard sensitive personal notes and credentials. It features seamless Firebase Authentication, instant local record manipulation, persistent auto-login sessions, and zero-latency reactive UI updates.",
  "architectureSummary": "Reactive client-side architecture combining Realm DB local persistence, Firebase cloud authentication, and Android ViewBinding.",
  "techStack": [
    "Android SDK",
    "Java",
    "Realm",
    "Firebase Authentication",
    "Firebase Realtime Database",
    "Material Components",
    "ViewBinding",
    "Gradle"
  ],
  "telemetryMatrix": {
    "projectType": "Native Mobile Application",
    "targetPlatform": "Android 7.0 to 12L (API 24-32)",
    "primaryDomain": "Personal Data & Credential Vault",
    "architecturePipeline": "Offline-First MVVM Reactive Architecture",
    "testingAndAudit": "Verified",
    "projectStatus": "Completed",
    "projectYear": "2022"
  },
  "desktopMobileProjectInfo": {
    "applicationType": "Native Mobile Application",
    "targetPlatform": "Android OS (API 24-32)",
    "developmentStatus": "Completed",
    "developmentYear": "2022",
    "applicationCategory": "Personal Data Management"
  },
  "desktopMobileBackground": "Users frequently struggle to securely manage and access confidential credentials, backup codes, and sensitive personal notes across mobile devices. Privena addresses this vulnerability by pairing offline embedded Realm storage for instant local accessibility with Firebase cloud identity verification to prevent unauthorized data access.",
  "desktopMobileProblemStatements": [
    {
      "title": "Vulnerability of Unsecured Plaintext Notes",
      "description": "Storing critical account credentials and API keys in standard note-taking apps exposes sensitive data to unauthorized local access and lack of dedicated vault protection.",
      "issueCode": "ISSUE_01"
    },
    {
      "title": "High Latency and Network Dependency in Cloud Storage",
      "description": "Traditional cloud-based note tools require active internet connections to view or edit emergency credentials, stalling workflows during network interruptions or transit.",
      "issueCode": "ISSUE_02"
    },
    {
      "title": "Cumbersome Session and Re-authentication Workflows",
      "description": "Frequent forced re-logins degrade mobile user experience, yet weak session management risks exposing stored credentials on unattended smartphones.",
      "issueCode": "ISSUE_03"
    }
  ],
  "desktopMobileObjectives": [
    {
      "title": "Deliver High-Speed Offline Storage",
      "description": "Implement embedded Realm database engine to execute sub-millisecond local CRUD operations without depending on network availability.",
      "targetTag": "TARGET_01"
    },
    {
      "title": "Ensure Secure Cloud Identity Verification",
      "description": "Integrate Firebase Authentication to provide enterprise-grade user onboarding, password hashing, and automated password reset recovery channels.",
      "targetTag": "TARGET_02"
    },
    {
      "title": "Build Reactive and Fluid User Interfaces",
      "description": "Utilize Android ViewBinding and RealmChangeListener to guarantee automatic, instantaneous RecyclerView synchronizations upon data mutation.",
      "targetTag": "TARGET_03"
    }
  ],
  "desktopMobileFeatures": [
    {
      "title": "Firebase Cloud Authentication & Password Reset",
      "description": "Enables secure user registration, email-password login, and automated reset email dispatch directly connected to Firebase backend.",
      "badge": "Security",
      "metric": "Instant Verification"
    },
    {
      "title": "High-Speed Realm Database Engine",
      "description": "Stores structured vault notes locally within an embedded Realm database instance sorted chronologically by creation timestamp.",
      "badge": "Local Storage",
      "metric": "Sub-millisecond CRUD"
    },
    {
      "title": "Reactive Real-time UI Synchronization",
      "description": "Leverages RealmChangeListener to automatically update the RecyclerView adapter upon note additions, modifications, or deletions.",
      "badge": "UI Architecture",
      "metric": "Zero Manual Refresh"
    },
    {
      "title": "Contextual Item Actions & Modals",
      "description": "Supports intuitive long-click popup menu triggers on note items, allowing seamless contextual editing and deletion.",
      "badge": "User Experience",
      "metric": "Single-Gesture Trigger"
    },
    {
      "title": "Persistent Auto-Login Session Caching",
      "description": "Uses Android SharedPreferences to remember authenticated user sessions, routing returning users directly from Splash to Dashboard.",
      "badge": "Session Cache",
      "metric": "3-Second Splash Route"
    }
  ],
  "desktopMobileInterfaceShowcase": [
    {
      "imageUrl": "/images/projects/privena_personal_data_management/image01.webp",
      "caption": "Secure onboarding and authentication gateway featuring registration, login, and self-service password reset flows.",
      "badge": "Auth Flow"
    },
    {
      "imageUrl": "/images/projects/privena_personal_data_management/image02.webp",
      "caption": "Personal vault dashboard displaying encrypted notes list, record creation form, and asynchronous update modal.",
      "badge": "Vault Management"
    }
  ],
  "desktopMobileUserFlow": {
    "summary": "The user launches Privena through the branded splash screen where cached SharedPreferences determine auto-login eligibility. Authenticated users land on the vault dashboard to immediately view, create, or update encrypted credential notes, while unauthenticated users complete rapid Firebase sign-in.",
    "steps": [
      {
        "step": "01",
        "title": "Launch and Session Resolution",
        "description": "Application initializes Realm and checks SharedPreferences autologin status during splash delay.",
        "actorOrNode": "Android System & Splash Activity"
      },
      {
        "step": "02",
        "title": "Authentication or Registration",
        "description": "User enters email and password; Firebase validates credentials and issues persistent session tokens.",
        "actorOrNode": "User & Firebase Auth"
      },
      {
        "step": "03",
        "title": "Vault Record Display",
        "description": "Dashboard fetches Realm notes ordered by creation time and renders them in RecyclerView.",
        "actorOrNode": "Realm Engine & UI Thread"
      },
      {
        "step": "04",
        "title": "Record Creation and Mutation",
        "description": "User submits new or edited note; Realm executes transaction and notifies adapter listeners.",
        "actorOrNode": "User & Realm Transaction"
      },
      {
        "step": "05",
        "title": "Session Termination",
        "description": "User taps logout to invoke Firebase sign-out, clear local session flags, and return to sign-in.",
        "actorOrNode": "User & Session Manager"
      }
    ]
  },
  "desktopMobileArchitecture": {
    "summary": "Privena is structured into decoupled presentation, local persistence, and remote authentication layers. ViewBinding connects Android Activity layouts to UI logic, Realm manages zero-copy local object persistence, and Firebase handles remote identity verification and user records.",
    "layers": [
      {
        "name": "Presentation Layer",
        "role": "Handles user interactions, UI view binding, and activity lifecycles",
        "tech": "Android Jetpack ViewBinding",
        "components": [
          "Splash",
          "Signin",
          "Signup",
          "Forgot",
          "Dashboard",
          "AddNoteActivity",
          "EditNoteActivity",
          "MyAdapter"
        ]
      },
      {
        "name": "Local Persistence Layer",
        "role": "Provides zero-latency embedded object database and preference storage",
        "tech": "Realm Mobile Database",
        "components": [
          "Realm Engine",
          "Note RealmObject",
          "RealmChangeListener",
          "SharedPreferences Session Cache"
        ]
      },
      {
        "name": "Remote Cloud Layer",
        "role": "Manages identity lifecycle, credential verification, and user profiles",
        "tech": "Firebase Services",
        "components": [
          "Firebase Authentication",
          "Firebase Realtime Database",
          "UserPersonal Model"
        ]
      }
    ]
  },
  "desktopMobileDataManagement": {
    "storageType": "Embedded Object-Oriented Realm Database",
    "stateEngine": "Reactive RealmChangeListener Observer Pattern",
    "offlineSyncStrategy": "Local-First Standalone Execution with Cloud Auth Guard",
    "cachingMechanism": "In-Memory Realm Cache & Persistent SharedPreferences"
  },
  "desktopMobilePlatformImplementation": [
    {
      "title": "Embedded Realm Native Engine Integration",
      "description": "Integrates io.realm Gradle plugin leveraging native C++ core binaries for high-efficiency zero-copy object queries directly in Android memory space.",
      "badge": "Native Storage"
    },
    {
      "title": "ViewBinding Memory-Safe Architecture",
      "description": "Eliminates runtime findViewById lookups through compile-time type-safe ViewBinding generation across all activities and viewholders.",
      "badge": "UI Pipeline"
    },
    {
      "title": "Asynchronous Transaction Threading",
      "description": "Dispatches database updates and background writes using executeTransactionAsync to guarantee stutter-free 60 FPS UI rendering.",
      "badge": "Concurrency"
    }
  ],
  "desktopMobileTechSpecs": {
    "programmingLanguage": "Java",
    "framework": "Android SDK",
    "localStorage": "Realm"
  },
  "desktopMobilePlatformSpecs": {
    "targetPlatform": "Android 7.0 Nougat Plus",
    "packageFormat": "Android Package Kit APK",
    "targetArchitecture": "Universal ARM and x86",
    "buildFootprint": "Under 15 Megabytes"
  }
}
```
