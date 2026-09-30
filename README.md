# Hello PWA

A small Progressive Web App built with plain HTML, CSS, and JavaScript.

## Features

- Web app manifest
- App icons for PWA installation
- Service worker registration
- Basic offline file caching
- Desktop and mobile screenshots for richer PWA install UI

## Project Structure

```text
hello-pwa/
├── app.js
├── index.html
├── manifest.json
├── service-worker.js
├── style.css
├── icons/
│   ├── icon-192.png
│   └── icon-512.png
└── screenshots/
    ├── desktop.png
    └── mobile.png
```

## Run Locally

This project should be served from a local web server. Do not open `index.html` directly from the file system, because service workers and PWA features need a proper origin such as `localhost`.

### Option 1: VS Code Live Server

1. Install the **Live Server** extension in VS Code.
2. Open this project folder in VS Code.
3. Right-click `index.html`.
4. Select **Open with Live Server**.
5. Open DevTools in Chrome and check **Application > Manifest**.

The app is expected to run at:

```text
http://localhost:5500
```

### Option 2: Python HTTP Server

If Python is installed, run:

```bash
python3 -m http.server 5500
```

Then open:

```text
http://localhost:5500
```

## Check PWA Status

In Chrome:

1. Open DevTools.
2. Go to the **Application** tab.
3. Check **Manifest** for icons, screenshots, and installability.
4. Check **Service workers** to confirm the service worker is registered.

If old files are still being used, go to **Application > Storage** and click **Clear site data**, then reload the page.

## Notes

- The icon files must match the sizes declared in `manifest.json`.
- The screenshots are used by Chrome for the richer install UI.
- The service worker cache name should be changed when cached assets are updated.
