# UniTask — Academic Homework Tracker

UniTask is a web app for keeping track of university assignments and deadlines.
You sign in with Google, and your tasks are saved in the cloud.

🔗 **Live website:** https://unitask-a9204.web.app

## Preview Version

The full app is private and only the owner's Google account can sign in. To let
others try it, the login screen has a **View Preview Version** button. It opens
the same app with sample Electrical Engineering courses and tasks.

- Changes stay in the browser's memory only. Nothing is saved to the database,
  and everything resets when you leave the preview or reload the page.
- You can add up to **30 tasks** and **5 subjects** per visit. Deleting,
  editing and marking tasks as completed are not limited.
- The preview cannot read or change the owner's data.

## Calendar

The **Calendar** tab sits above **All Courses** and opens a full-width month
calendar of all tasks. It works like a course tab: opening it deselects the
current tab, and clicking **All Courses** or any course closes it. Tasks appear
on their due date.

- Weeks start on Sunday and each row is one week.
- Scroll up or down to move between months; there are no next/previous buttons.
- Months alternate a subtle background tint, a thin line marks where each month
  starts, and days outside the month in view are dimmed.
- Day cells stay square: if a day has more than 3 tasks, the cell shows 2 and a
  "+N more tasks" line.
- Click any day to open a popup listing every task due that day, with full details
  and editing, plus an **Add task on this day** button.
- **Today** jumps back to the current month.

## ⚠️ Disclaimer

This project was made as a **homework assignment**. The assignment asked for the
website to be published with **GitHub Pages**.

I chose to host it on **Firebase Hosting** instead, because the app needs to
**store user data**: accounts and saved tasks. GitHub Pages only serves static
files and has no database or user sign-in. Firebase gives me hosting,
**Firebase Authentication** (Google sign-in) and a **Cloud Firestore** database
in one place.

The full source code is still published here on GitHub. Only the live
deployment runs on Firebase.

## Tech Stack

- HTML, CSS and JavaScript (single page: `index.html`)
- Firebase Hosting
- Firebase Authentication (Google sign-in)
- Cloud Firestore

## Project Structure

| File              | Purpose                               |
|-------------------|---------------------------------------|
| `index.html`      | The whole app (UI and logic)          |
| `firebase.json`   | Firebase Hosting and Firestore config |
| `firestore.rules` | Firestore security rules              |
| `.firebaserc`     | Firebase project alias                |

## Deploying

```bash
npm install -g firebase-tools
firebase login
firebase deploy
```
