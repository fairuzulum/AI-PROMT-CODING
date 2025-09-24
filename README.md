# AI-PROMT-CODING


You are an expert Android developer specializing in Kotlin, Jetpack Compose, and modern Android architectures. I need your help to build a personal Android app from scratch. The app is for my own use only, so no need for publishing or advanced security beyond basics. It should have two main sections: one for financial tracking (income and expenses) and one for notes (tasks, personal notes, passwords, etc.). I want to add more features later, so make it scalable.

Key Requirements:
- App Name: Personal Tracker (or suggest a better one).
- UI: Simple and intuitive. Use a bottom navigation bar to switch between "Finance" and "Notes" screens.
- Finance Section: 
  - Add/edit/delete transactions (income/expense with amount, date, category, description).
  - Display list of transactions (sortable by date/category).
  - Show total balance, monthly summary (use charts if easy, like MPAndroidChart).
- Notes Section:
  - Add/edit/delete notes (title, content, tags/categories like "task", "password", "memo").
  - Search and filter notes.
  - For passwords, encrypt them simply (using Android Cipher or Keystore).
- Data Storage: Use Room Database as local primary storage for speed and offline access. Tables: One for Transactions (id, type[income/expense], amount, date, category, desc), one for Notes (id, title, content, category, timestamp).
- Sync: Background sync to Google Sheets daily or on-demand. Use WorkManager to schedule. Export data as CSV/JSON and append to Sheets via Google Sheets API v4. One-way sync (app to Sheets) is fine for now. Handle authentication with Google Sign-In.
- Performance: App must be super fast, no lag even with thousands of entries. Use Paging for lists, Coroutines/Flow for async ops.
- Other: Offline-first, handle errors gracefully (e.g., no network for sync), basic theme (light/dark mode if possible).

Tech Stack:
- Language: Kotlin only.
- IDE: Android Studio (latest version).
- UI: Jetpack Compose (no XML views).
- Architecture: MVVM with Hilt for DI.
- Libraries: 
  - Room for DB.
  - Navigation Component for screens.
  - Coroutines and Flow for reactive data.
  - WorkManager for sync.
  - Google API Client or Retrofit for Sheets API.
  - MPAndroidChart or Compose Charts for finance visuals.
  - No Firebase; stick to local + Sheets.

Step-by-Step Guidance:
1. Setup the project: Create a new Android Studio project with Compose. Add dependencies in build.gradle (list them out).
2. Implement Room DB: Define entities, DAO, Database class. Provide code examples.
3. Build UI: Compose screens for Finance and Notes. Use LazyColumn for lists, Dialog for add/edit.
4. ViewModels: For each screen, handle data flow from Repo to UI.
5. Repository: Abstract data source (Room + potential future cloud).
6. Sync Implementation: Setup WorkManager worker that queries Room, formats data, and calls Sheets API. Include auth setup.
7. Testing: Suggest basic unit tests for DAO and integration tests.
8. Optimization: Tips for handling large data, like indexing in Room.
9. Full Code: If possible, provide a GitHub-like structure or key files' code.

Please guide me from zero: Start with project setup, then code snippets for each part. Ask for clarification if needed, but assume I'm a pro dev who can follow along. Output in code blocks for easy copy.
