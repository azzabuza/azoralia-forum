# Web Forum Application

This is a simple web-based forum application built using HTML, CSS, and JavaScript. It allows users to post threads, view other users' threads, and interact in a real-time discussion forum. The application is integrated with Firebase for authentication and database storage.

## Features
- User authentication using Firebase.
- Real-time posting and retrieval of threads.
- Responsive design, accessible on mobile and desktop.
- Simple and easy-to-use interface.

## Technologies Used
- **HTML5**: Structure of the web application.
- **CSS3**: Styling the web application.
- **JavaScript**: Handling interactivity and Firebase integration.
- **Firebase**: Backend for authentication and real-time database.

## Requirements
Before running the application, ensure you have the following:
- A Firebase account with a created project.
- Firebase Realtime Database enabled in your Firebase project.
- A web browser that supports modern JavaScript (Chrome, Firefox, Edge, etc.).

## Firebase Setup
To set up Firebase for this application, follow these steps:
1. **Create a Firebase project**:
   - Go to the [Firebase Console](https://console.firebase.google.com/).
   - Create a new project or use an existing one.
2. **Enable Firebase Realtime Database**:
   - In the Firebase Console, go to the "Realtime Database" section.
   - Click "Create Database" and set the rules to allow read and write access during development:
     ```json
     {
       "rules": {
         ".read": "auth != null",
         ".write": "auth != null"
       }
     }
     ```

3. **Enable Firebase Authentication**:
   - In the Firebase Console, go to the "Authentication" section.
   - Enable Email/Password authentication.
4. **Get Firebase configuration**:
   - Go to your Firebase project settings.
   - Under "Your apps" section, add a web app and copy the Firebase configuration details.

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/web-forum-app.git
cd web-forum-app
