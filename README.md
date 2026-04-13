# YouTube Tracker

A clean, dark-themed web app to track YouTube videos you want to watch, are currently watching, and have finished — all saved locally in your browser with no account or server needed.

## Features

- **Three-stage workflow** — Upcoming → In Progress → Watched
- **Embedded player** — watch videos in-app without leaving the page
- **Real progress tracking** — progress bar tied to actual watch time via the YouTube IFrame API
- **Auto-promotion** — watching a video moves it from Upcoming to In Progress automatically; finishing moves it to Watched
- **Resume where you left off** — reopening a video seeks to your last position
- **Categories** — create color-coded categories and filter your list by them
- **Notes** — add personal notes to any video
- **Search** — filter videos by title in real time
- **Import / Export** — back up and restore your list as a JSON file

## Usage

No installation or build step required. Just open `index.html` in any modern browser.

```
youtube-tracker/
└── index.html   ← open this
```

All data is stored in `localStorage` — your list persists across page refreshes and browser restarts, scoped to the local file.

## Workflow

1. Paste a YouTube URL or video ID into the input and click **+ Add Video**
2. The video lands in **Upcoming**
3. Click **▶** to open the embedded player — the video automatically moves to **In Progress**
4. Your progress is tracked as you watch and saved when you pause or close
5. When the video ends it moves to **Watched** automatically, or you can click **Mark Watched** manually

## Tech Stack

| Layer | Technology |
|---|---|
| UI | HTML + CSS (no framework) |
| Logic | Vanilla JavaScript |
| Storage | `localStorage` |
| Video | YouTube IFrame Player API |
| Metadata | YouTube oEmbed API (no API key needed) |
| Thumbnails | YouTube image CDN |

## Screenshots

> Upcoming, In Progress, and Watched tabs with category filters, progress bars, and the embedded player.

## License

MIT
