# Chat Out

A real-time chat application built with React Native, Expo, and Firebase.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Firebase Configuration](#firebase-configuration)

## Features

- **Real-time messaging:** Communicate instantly with friends and colleagues.
- **User authentication:** Sign up and login with email and password using Firebase Authentication.
- **Group chats:** Create and join group conversations.
- **Offline support:** Messages are cached and sent when the connection is restored.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Node.js (>=14.x)
- Expo CLI (>=5.x): Install via `npm install -g expo-cli`
- Firebase project: Set up a Firebase project with Authentication, Firestore, and Storage enabled.

## Installation

1. **Clone the repository:**

    ```sh
    git clone https://github.com/malikraheel12/Chat-Out.git
    cd Chat-Out
    ```

2. **Install dependencies:**

    ```sh
    npm install
    ```

3. **Configure Firebase:**

    - Follow the [Firebase Configuration](#firebase-configuration) section to set up your Firebase project.

4. **Run the app:**

    ```sh
    expo start
    ```

    This will start the Expo development server. You can then run the app on an iOS or Android simulator, or on a physical device using the Expo Go app.

## Usage

1. **Sign up or log in:**
    - Users can sign up with an email and password or log in with existing credentials.

2. **Start a chat:**
    - Navigate to the chat screen and start a new conversation or join an existing one.

3. **Send messages:**
    - Type a message and send it in real-time. Users will receive notifications for new messages.

## Firebase Configuration

To connect the app to Firebase, follow these steps:

1. **Create a Firebase project:**
    - Go to the [Firebase Console](https://console.firebase.google.com/) and create a new project.

2. **Enable Authentication:**
    - Go to the "Authentication" section and enable Email/Password authentication.

3. **Set up Firestore:**
    - Go to the "Firestore Database" section and create a database. Set the security rules as needed.

4. **Enable Storage:**
    - Go to the "Storage" section and enable Firebase Storage for media uploads.

5. **Add Firebase configuration to your app:**
    - Download the `google-services.json` (for Android) and `GoogleService-Info.plist` (for iOS) from your Firebase project settings.
    - Place them in the appropriate directories:
        - `android/app/google-services.json`
        - `ios/GoogleService-Info.plist`

6. **Update Firebase configuration:**

    Create a `firebaseConfig.js` file in the `src/config` directory with your Firebase credentials:

    ```js
    // src/config/firebaseConfig.js
    import { initializeApp } from 'firebase/app';

    const firebaseConfig = {
      apiKey: "YOUR_API_KEY",
      authDomain: "YOUR_AUTH_DOMAIN",
      projectId: "YOUR_PROJECT_ID",
      storageBucket: "YOUR_STORAGE_BUCKET",
      messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
      appId: "YOUR_APP_ID",
    };

    const app = initializeApp(firebaseConfig);
    export default app;
    ```
