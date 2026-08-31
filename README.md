# Gmail Attachment Cleaner

A browser-based tool to find and trash Gmail emails with large attachments. Runs entirely in your browser — no backend, no data stored anywhere except your own browser's `localStorage`.

## Features

- Scan Gmail for attachments above a chosen size (5 MB, 10 MB, 20 MB, 50 MB, 100 MB, or custom)
- See every matching thread with attachment filename, file type, and exact size
- Expand any thread to inspect individual files before deciding
- Uncheck threads you want to keep — only checked ones go to Trash
- Moved threads stay in Trash for 30 days and can be restored

## Setup

### 1. Google Cloud project

1. Go to [Google Cloud Console](https://console.cloud.google.com/) and create a project.
2. Enable the **Gmail API** (APIs & Services → Library).
3. Configure the **OAuth consent screen** (External → add your email → add scope `https://www.googleapis.com/auth/gmail.modify` → add yourself as a Test User).
4. Create an **OAuth 2.0 Client ID** (Credentials → Web application).
5. Under *Authorized JavaScript origins*, add your live domain — e.g. `https://gmail-cleaner.vercel.app`.
6. Copy the **Client ID**.

### 2. Use the tool

Open the deployed URL, paste your Client ID, click **Connect**, then **Sign in with Google**.

## Deploy

Click the button below or import this repo in [vercel.com/new](https://vercel.com/new).

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/YOUR_USERNAME/gmail-cleaner)

## Privacy

Your OAuth Client ID is stored only in your browser's `localStorage`. No data leaves your device except the Gmail API calls made directly to Google's servers with your own access token.

## License

MIT
