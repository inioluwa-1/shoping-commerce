# Firebase Authentication Setup Guide

## Step 1: Create a Firebase Project

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Click "Add project" or "Create a project"
3. Enter your project name (e.g., "shopping-commerce")
4. Disable Google Analytics (optional) or configure it
5. Click "Create project"

## Step 2: Register Your Web App

1. In your Firebase project dashboard, click the **Web icon** (`</>`)
2. Register your app with a nickname (e.g., "E-Commerce Store")
3. Don't check "Firebase Hosting" (unless you want to use it)
4. Click "Register app"
5. Copy the Firebase configuration object that looks like this:

```javascript
const firebaseConfig = {
  apiKey: "AIzaSyXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  authDomain: "your-project.firebaseapp.com",
  projectId: "your-project",
  storageBucket: "your-project.appspot.com",
  messagingSenderId: "123456789012",
  appId: "1:123456789012:web:abcdef123456"
};
```

## Step 3: Enable Authentication Methods

1. In Firebase Console, click **"Authentication"** in the left sidebar
2. Click **"Get started"** if this is your first time
3. Go to the **"Sign-in method"** tab
4. Enable the following providers:

### Email/Password Authentication
- Click on "Email/Password"
- Toggle "Enable" to ON
- Click "Save"

### Google Sign-In (Optional but recommended)
- Click on "Google"
- Toggle "Enable" to ON
- Enter a support email for your project
- Click "Save"

## Step 4: Configure Your App

Replace the Firebase configuration in the following files:

### 1. login.html
Find this section around line 165:
```javascript
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_AUTH_DOMAIN",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_STORAGE_BUCKET",
    messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
    appId: "YOUR_APP_ID"
};
```

Replace it with your actual Firebase config from Step 2.

### 2. index.html
Find the same section around line 90 and replace with your config.

### 3. admin.html
Find the same section around line 118 and replace with your config.

## Step 5: Test Your Authentication

1. Open `login.html` in your browser
2. Try creating a new account with email/password
3. Try signing in with the account you created
4. Try signing in with Google (if enabled)
5. You should be redirected to `index.html` after successful login
6. Test the logout functionality

## Security Rules (Optional but Recommended)

If you plan to use Firebase Firestore or Storage, set up security rules:

### Firestore Rules
```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```

### Storage Rules
```
rules_version = '2';
service firebase.storage {
  match /b/{bucket}/o {
    match /{allPaths=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```

## Features Implemented

✅ **Email/Password Sign Up** - Users can create accounts with email and password
✅ **Email/Password Sign In** - Users can log in with their credentials
✅ **Google Sign-In** - One-click sign in with Google account
✅ **Authentication Protection** - Pages redirect to login if user is not authenticated
✅ **User Display** - Shows logged-in user's name in the navigation
✅ **Logout Functionality** - Users can sign out securely
✅ **Password Visibility Toggle** - Show/hide password while typing
✅ **Form Validation** - Client-side validation with helpful error messages
✅ **Persistent Login** - Users stay logged in across page refreshes

## Troubleshooting

### "Firebase: Error (auth/configuration-not-found)"
- You need to replace the Firebase config with your actual project credentials

### "Firebase: Error (auth/api-key-not-valid)"
- Double-check that you copied the complete API key from Firebase Console

### Google Sign-In Popup Blocked
- Make sure your browser allows popups for your local server
- Check if you've enabled Google Sign-In in Firebase Console

### Users Not Redirecting After Login
- Check the browser console for errors
- Make sure all three files have the same Firebase config
- Verify your Firebase project is active

## Local Development

To test locally, you can use:
- **VS Code Live Server** extension
- **Python**: `python -m http.server 8000`
- **Node.js**: `npx http-server`
- **PHP**: `php -S localhost:8000`

Then open: `http://localhost:8000/login.html`

## Next Steps

Consider adding:
- Password reset functionality
- Email verification
- User profile management
- Social login (Facebook, Twitter, etc.)
- Two-factor authentication
- Store user data in Firestore

## Support

For Firebase documentation, visit:
- [Firebase Auth Docs](https://firebase.google.com/docs/auth)
- [Firebase Console](https://console.firebase.google.com/)
- [Firebase JavaScript SDK Reference](https://firebase.google.com/docs/reference/js)
