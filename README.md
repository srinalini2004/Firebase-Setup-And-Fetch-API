# Book Management Web App (Firebase)

## Overview
This is a simple Book Management Web Application that uses **Firebase Firestore** as the backend to store and manage book data. It supports adding, updating (author), deleting books, and displays real-time updates. A client-side search bar filters books in real-time. The UI shows books in card format (3 per row on desktop).

## Features
- Add new books (Title, Author, Price, Image URL)
- Real-time list sync using Firestore `onSnapshot`
- Update Author for a book
- Delete a book
- View Details modal for a book
- Search by title or author (real-time)
- Seeds 5 sample books automatically if `books` collection is empty

## How to set up
1. Create a new Firebase project at https://console.firebase.google.com/.
2. In the project, go to **Firestore Database** and create a database (start in test mode for development).
3. In **Project Settings > Your apps**, add a Web app and copy the Firebase config object.
4. Replace the `firebaseConfig` object in `index.html` with your project's config.
5. Ensure Firestore rules allow reads/writes for development, or configure auth appropriately.

## Run locally
1. Place `index.html` in a folder and open it in a modern browser (Chrome/Edge/Firefox).
2. The app will connect to your Firestore project and seed sample books if none exist.
3. Use the sidebar form to add books. Use card buttons to update/delete/view.

## Files to submit
- `index.html`
- `README.md`

## Notes
- This uses Firebase v9 (modular) via CDN imports.
- For production, secure Firestore rules and consider using a build system / bundler.
- The "Clear All Books" button will delete every document in the `books` collection — use with care.

