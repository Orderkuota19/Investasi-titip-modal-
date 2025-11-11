# Invest-Bot (Telegram Admin + API) - Ready to Deploy

This project contains a Telegram Admin bot integrated with an Express API and Firebase Firestore.
It notifies the admin on top-ups from the website and allows admin commands.

## Files
- `index.js` - main server (Express API + Telegram bot)
- `firebase.js` - Firebase initialization (reads base64 JSON from env)
- `public/index.html` - example frontend that calls `/api/topup`
- `.env.example` - example environment variables
- `package.json` - dependencies & start script

## Setup (local)
1. Clone or unzip this project.
2. Create a Firebase project and generate a service account JSON file:
   - Firebase Console → Project Settings → Service Accounts → Generate new private key
   - Save the JSON file (e.g. `serviceAccountKey.json`)
3. Convert the JSON to base64 (do NOT commit it):
   - macOS / Linux:
     ```
     base64 serviceAccountKey.json > serviceKey.b64
     ```
   - Windows (PowerShell):
     ```
     [Convert]::ToBase64String([IO.File]::ReadAllBytes("serviceAccountKey.json")) > serviceKey.b64
     ```
   - Open `serviceKey.b64` and copy its contents.
4. Create `.env` in project root and paste:
   ```
   BOT_TOKEN=your_new_token_from_botfather
   ADMIN_CHAT_ID=your_telegram_chat_id
   PORT=10000
   FIREBASE_KEY_BASE64=PASTE_THE_BASE64_STRING_HERE
   ```
5. Install dependencies:
   ```
   npm install
   ```
6. Run:
   ```
   npm start
   ```
7. Visit the frontend example: open `public/index.html` in your browser (or host it).

## Deploy to Render / Railway
- Push repo to GitHub.
- Create a new Web Service on Render and connect the repo.
- Provide environment variables in Render's dashboard (BOT_TOKEN, ADMIN_CHAT_ID, FIREBASE_KEY_BASE64, PORT).
- Deploy.

## Security notes
- Revoke and recreate the bot token if you accidentally exposed it.
- Never commit `.env` or your Firebase key to public repositories.
