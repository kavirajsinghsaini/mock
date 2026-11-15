# SSC Study Hub — Royal Edition

## Included
- `index.html` — original 53 CGL reasoning mocks, their embedded question data and quiz engine, with a redesigned dashboard.
- A single premium royal-night theme (deep navy, charcoal and champagne gold) is used throughout. The default display name is **Kaviraj**; change it any time under **Settings → Display name**. The selected name is saved on that device.
- `manifest.webmanifest` — install metadata.
- `sw.js` — versioned app-shell cache and offline navigation fallback.
- `icon-192.png`, `icon-512.png` — PWA icons.

## Deploy to GitHub Pages
1. Create a GitHub repository and upload all files from this folder to the repository root (keep the filenames unchanged).
2. In **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
3. Wait for GitHub Pages to publish the site. Open the published HTTPS URL once while online.

## Install on Android
1. Open the published URL in Chrome.
2. Use Chrome's menu and choose **Install app** or **Add to Home screen** when offered.
3. Launch SSC Study Hub from the home screen.

## Important notes
- The dashboard click-handler startup issue is fixed: the original script expected a resume control that was missing from the redesigned markup. The compatibility control is now present, so initialization can complete and navigation, mock rendering, search, filters, and test launching can register. The shell now uses one consistent dark-and-gold theme; the old light/dark switch has been removed. The profile display name defaults to Kaviraj and can be changed in Settings.
- The 53 embedded mock payloads, original question data, original quiz engine, and original localStorage keys are retained. The visual shell and dashboard presentation have been changed.
- The original mock engine provides per-mock answer/session persistence. The outer page does not expose a unified saved-question index; the SAVED page explains this and directs you to the original in-mock controls rather than inventing a new bookmark store.
- Dashboard counts are calculated from the original per-mock state. Accuracy, best score, and subject-wise analytics are not shown because the source dashboard does not expose reliable aggregate values for them.
- Offline availability begins only after a successful online visit and successful service-worker installation. Browser/device-specific installation and offline behaviour should be verified after deployment.
