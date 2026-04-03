# YouTube Assistant (Search + Speed + CC Language)

A lightweight browser-based app for in-page YouTube interaction:
- Search YouTube videos using the YouTube Data API v3
- Play video in an embedded player
- Control playback speed (0.25x to 2x)
- Choose closed caption language preference (Malayalam, English, Hindi)
- Save YouTube API key locally in browser storage

## Features

- Search box for video queries
- Video thumbnails grid produced from API results
- Video playback inside `iframe` with JavaScript control
- Playback speed selector (`#speed`)
- CC language selector (`#lang`)
- Persistent API key in `localStorage` (secure by not exposing in code)
- API key help modal with setup steps
- 153 error guidance for file:// origin (local server recommended)

## Setup

1. Clone or download repository.
2. Obtain a YouTube Data API v3 key from Google Cloud Console:
   - `APIs & Services > Library` → enable `YouTube Data API v3`
   - `APIs & Services > Credentials` → create API key
3. Open `index.html` in browser from a local HTTP server (recommended):
   - `python -m http.server 8000`
   - `http://localhost:8000`
4. Paste API key in the "Device Configuration" box.
5. Click "Save to Browser".

## Usage

1. Enter a search term (e.g., "Science experiments") and press Enter or click `SEARCH`.
2. Click a video card to load and play.
3. Select playback speed from dropdown.
4. Select caption language from dropdown.

## Notes

- Subtitle/Captions language depends on availability from the selected video.
- Playback speed may fall back to the nearest available YouTube playback rate.
- If you get `Error 153`, run from a local web server instead of `file://`.

## Customize

- Modify the video search max result count in `searchVideos()`.
- Extend language list in `<select id="lang">`.

## License

MIT.

