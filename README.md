# Flutter Firebase Authentication App

This is a Flutter application that demonstrates Firebase Authentication with email/password login and signup functionality.

## Project Structure

```
lib/
├── providers/
│   └── auth_provider.dart     # Manages authentication state
├── screens/
│   ├── login_screen.dart      # Login screen
│   ├── signup_screen.dart     # Signup screen
│   └── home_screen.dart       # Home screen after authentication
├── firebase_options.dart      # Firebase configuration
└── main.dart                  # App entry point
```

## Important Files and Their Purpose

### 1. Authentication Files
- `lib/screens/login_screen.dart`
  - Contains the login form
  - Fields:
    - Email
    - Password
  - Link to signup screen

- `lib/screens/signup_screen.dart`
  - Contains the signup form
  - Fields:
    - Email
    - Password
    - First Name
    - Last Name
  - Link back to login screen

- `lib/providers/auth_provider.dart`
  - Manages authentication state using Provider package
  - Handles:
    - User signup
    - User login
    - User logout
    - Current user state

### 2. Home Screen
- `lib/screens/home_screen.dart`
  - Displayed after successful authentication
  - Shows user information
  - Contains logout button

### 3. Configuration Files
- `lib/firebase_options.dart`
  - Contains Firebase configuration
  - You need to replace placeholder values with your Firebase project details

- `web/index.html`
  - Contains web-specific Firebase configuration
  - Required for web deployment

## Setup Instructions

1. **Prerequisites**
   - Flutter SDK installed
   - Firebase account
   - Firebase CLI (optional)

2. **Firebase Setup**
   - Create a new project in [Firebase Console](https://console.firebase.google.com/)
   - Add an Android/iOS/Web app to your Firebase project
   - Download configuration files:
     - For Android: `google-services.json` → place in `android/app/`
     - For iOS: `GoogleService-Info.plist` → place in `ios/Runner/`
     - For Web: Update configuration in:
       - `lib/firebase_options.dart`
       - `web/index.html`

3. **Project Setup**
   ```bash
   # Clone the repository (if applicable)
   git clone <repository-url>

   # Navigate to project directory
   cd login_app

   # Install dependencies
   flutter pub get

   # Run the app
   flutter run
   ```

4. **Firebase Configuration**
   Replace the placeholder values in `lib/firebase_options.dart`:
   ```dart
   return const FirebaseOptions(
     apiKey: 'YOUR-API-KEY',
     appId: 'YOUR-APP-ID',
     messagingSenderId: 'YOUR-SENDER-ID',
     projectId: 'YOUR-PROJECT-ID',
     authDomain: 'YOUR-PROJECT.firebaseapp.com',
     storageBucket: 'YOUR-PROJECT.appspot.com',
   );
   ```

## Features

1. **Authentication**
   - Email/Password Sign Up (separate screen)
   - Email/Password Login (separate screen)
   - Logout functionality
   - Navigation between login and signup screens

2. **User Information**
   - Display user's name and email
   - Persistent authentication state

## Package Dependencies
- `firebase_core`: Firebase initialization
- `firebase_auth`: Authentication services
- `provider`: State management
- `google_fonts`: Custom fonts (optional)

## Common Issues and Solutions

1. **Firebase Configuration**
   - Make sure all configuration files are in the correct locations
   - Verify that all Firebase configuration values match your project

2. **Web Platform**
   - Ensure Firebase JS SDK is properly loaded in `index.html`
   - Check browser console for any JavaScript errors

3. **Android Platform**
   - Verify `google-services.json` is in `android/app/`
   - Check Android Studio for any Gradle sync issues

4. **iOS Platform**
   - Ensure `GoogleService-Info.plist` is added to Runner in Xcode
   - Check for any CocoaPods installation issues

## Contributing
Feel free to submit issues and enhancement requests!

## License
This project is licensed under the MIT License - see the LICENSE file for details
