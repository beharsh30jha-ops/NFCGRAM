# NFC Username Chat — Final Test Build v0.3

A username-first messaging app prototype with a polished four-tab UI.

## Included in this build

### Authentication
- App launch shows **Login** and **Sign up**
- Login requires username + password
- Sign up requires a unique username + password
- Optional Gmail address is collected for future account recovery
- Duplicate usernames show **Username already taken**
- Local demo account persistence
- Forgot-password recovery flow is included as a **local test-mode flow**

> Important: real Gmail password-reset emails require a backend (Firebase/Supabase/etc.). This ZIP is intentionally backend-free so the APK can be tested immediately. The recovery UI is ready to be connected to Firebase Auth later.

### Main app
Four bottom sections matching the supplied reference:
1. Chats
2. Contacts
3. Settings
4. Profile

### Chat
- Username search
- 1-to-1 conversations
- Send messages
- Reply
- Reaction demo
- Delete for me
- Delete for everyone
- Block / unblock
- Archive / unarchive chats
- Archived chats section

### UX / design
- Animated day/night home background
- Light / dark / system theme
- Multiple aesthetic wallpapers
- Premium theme preview / local premium toggle
- Smooth animated transitions
- Haptic-style UI feedback where supported by Flutter widgets
- Empty states and polished cards

## Run
```bash
flutter pub get
flutter run
```

## Build APK
```bash
flutter build apk --debug
```

A GitHub Actions workflow is included and will create a debug APK artifact.

## Backend phase
The next phase should replace the local demo repository with a real backend:
- Firebase Authentication (username mapping + email recovery)
- Firestore
- Firebase Storage
- Security Rules
- Real push notifications
- Real online/offline presence

Do not put private service-account credentials in GitHub.


## Final test-build notes
- Usernames are case-insensitive.
- Built-in demo usernames are reserved, so signing up as `@lily`, `@baka`, etc. correctly reports **Username already taken**.
- Passwords are stored only in the local test database in this prototype; this is not production authentication.
