# Z.ai Auto Retry

Automatically retries failed **GLM-5.2** requests on Z.ai during peak hours.

When Z.ai displays the **"Currently in peak hours"** popup, this script will:

* Detect the popup automatically.
* Close the popup.
* Wait for the interface to recover.
* Click the send button again.
* Notify the user that a retry is occurring.

## Features

* 🔄 Automatic retry during GLM-5.2 peak hours
* ❌ Automatically closes the peak-hours popup
* 🔔 Toast notifications
* 📝 Console logging for debugging
* ▶️ One-click start
* ⏹️ Click again to stop
* 📌 Persistent status indicator

## Installation

### Bookmarklet
The code is in `bookmark.js`

1. Open the included `index.html` page, or the [Live Page](https://eman225511.github.io/Z.ai-Auto-Retry/)
2. Drag the **"Z.ai Auto Retry"** button to your bookmarks bar.
3. Open Z.ai.
4. Click the bookmark to enable auto retry.

Click the bookmark again to disable it.

### Console
The code is in `console.js`

You can also paste the script directly into your browser's developer console.

1. Open Z.ai.
2. Press `F12`.
3. Open the **Console** tab.
4. Paste the script and press Enter.

## How It Works

The script continuously watches the page for changes using a `MutationObserver`.

When it detects a dialog containing:

```text
Currently in peak hours
```

and

```text
GLM-5.2
```

it will:

1. Close the popup.
2. Wait for the send button to become available.
3. Click the send button automatically.

## Status Indicator

A small indicator appears in the bottom-right corner while the script is active.

States:

* 🟢 **Auto Retry ON** — Script is running.
* 🔄 **Retrying...** — The script is currently retrying a message.

## Notifications

Toast notifications are displayed when:

* The script starts.
* A retry is triggered.
* The script stops.

## Console Logs

The script logs important events to the browser console.

Example:

```text
[Z.ai Auto Retry] Started
[Z.ai Auto Retry] Peak popup detected
[Z.ai Auto Retry] Closing popup
[Z.ai Auto Retry] Clicking send button
[Z.ai Auto Retry] Retry sent
```

## Disclaimer

This project is an unofficial utility and is not affiliated with or endorsed by Z.ai.

Use at your own risk. Website updates may require script updates in the future.

## License

MIT License
