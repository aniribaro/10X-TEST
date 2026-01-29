# 10X Accountability Coach - Landing Page

Standalone landing page that can run independently on port 3001.

## Quick Start

```bash
npm start
```

This will serve the landing page at **http://localhost:3001**

## Features

- Runs independently from the main app
- Checks if the main app (localhost:3000) is running before launching
- Shows helpful error dialog if app is not running
- Beautiful, responsive design

## App Availability Check

When users click "Launch App", the landing page will:

1. Check if the main app is running at localhost:3000
2. If running: Opens the app directly
3. If not running: Shows a dialog with instructions on how to start the app

## Running Both Together

**Terminal 1 - Main App:**
```bash
cd ui && npm run dev
# Runs at localhost:3000
```

**Terminal 2 - Landing Page:**
```bash
cd premium-white-label-kit/landing && npm start
# Runs at localhost:3001
```

## Customization

Edit the following files to customize the landing page:

- `index.html` - Content and structure
- `styles.css` - Styling and colors
- `script.js` - Interactivity and app check logic

---

**Developed by Team 10X** | Powered by OpenAnalyst
