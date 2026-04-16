# TuckShop POS

A robust, desktop-native Point of Sale (POS) application designed specifically to manage sales, track inventory, and streamline daily operations for campus facilities.

---

## Features

- **Sales & Khaata Management** – Process transactions quickly with an intuitive interface.
- **Inventory Tracking** – Real-time synchronization of stock levels and product details.
- **Barcode Scanner Integration** – Rapid item entry and checkout workflows tailored for high-traffic environments.
- **Cross-Platform Desktop App** – Packaged as an executable for Windows and macOS, running entirely as an independent desktop application.

---

## Tech Stack

This project is built using a modern desktop and web development stack:

| Layer | Technology |
|---|---|
| Frontend | React 18, Vite |
| Routing | React Router v7 |
| Desktop Framework | Electron 30 (`electron-builder`) |
| Backend / Database | Firebase 11 |
| UI / Styling | Material-UI (MUI) & Emotion |

---

## Getting Started

### Prerequisites

- Node.js (v18 or higher recommended)
- `npm` or `yarn`

### Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd tuckstack
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

---

## Development

To start the application in development mode with hot-reloading for both the React frontend and the Electron main process, run:

```bash
npm run electron:dev
```

> This uses `concurrently` to run the Vite dev server and the Electron app simultaneously.

If you only need to work on the web view in the browser without spinning up the desktop app:

```bash
npm run dev
```

---

## Build and Packaging

To compile the React code and package the Electron application into a distributable format:

1. Build the web assets and test the production Electron build locally:

   ```bash
   npm run electron:build
   ```

2. Pack the application for distribution (creates executables / DMG):

   ```bash
   npm run electron:pack
   ```

   The packaged outputs (e.g. `.exe` for Windows NSIS or `.dmg` for macOS) will be generated in the `release/` directory as defined in `package.json`.

---

## Firebase Configuration

This application relies on Firebase for real-time database and backend services. Ensure your `src/firebase.js` is properly configured with your project's credentials before running or building.

---

