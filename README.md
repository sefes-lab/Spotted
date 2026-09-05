# Spotted! 🔦
### License Plate Spotter Game — PWA Edition

A progressive web app for spotting license plates on road trips. Works offline, installable on iOS and Android.

---

## Files

| File | Purpose |
|------|---------|
| `index.html` | Main app — all game logic, UI, and D3 map |
| `manifest.json` | PWA manifest — name, icons, display mode |
| `sw.js` | Service worker — offline caching |
| `icon-192.png` | App icon (Android, PWA) |
| `icon-512.png` | App icon large (splash screen) |
| `apple-touch-icon.png` | iOS home screen icon |

---

## Deployment

Drop all files into any static web host:

**Netlify** — drag the folder into netlify.com/drop  
**GitHub Pages** — push to a repo, enable Pages  
**Vercel** — `vercel --prod` in the folder  
**Local** — `npx serve .` or `python3 -m http.server 8080`

> ⚠️ Must be served over **HTTPS** (or localhost) for the service worker and PWA install prompt to work.

---

## Installing on Device

**iOS (Safari):** Open the URL → Share → Add to Home Screen  
**Android (Chrome):** Open the URL → menu → Add to Home Screen  
**Desktop Chrome/Edge:** Address bar install icon appears automatically

---

## Game Features

- 🗺️ **Spot Runs** — create named trips, track across multiple sessions
- 🔦 **Spot Grid** — tap any state tile to log a sighting
- 📋 **Spot Log** — full sighting history, filterable and sortable
- 🗺️ **D3 Map** — real US map colored by point value (cool=close, hot=far)
- 🏆 **Spotter HQ** — leaderboard, stats, 17 achievements
- 👥 **Multi-spotter** — multiple players per run, each sighting credited
- ♾️ **Multi-sighting** — same state can be spotted many times, each scores
- 🌡️ **Dynamic scoring** — point values auto-calculate from home state distance
- 💾 **Offline** — fully playable with no connection after first load

---

## PWA Checklist

- ✅ HTTPS required (or localhost)
- ✅ manifest.json with valid icons
- ✅ Service worker with offline cache
- ✅ apple-mobile-web-app meta tags
- ✅ Responsive viewport
- ✅ Theme color
- ⏳ Push notifications (future)
- ⏳ Real PNG icons with app artwork (replace placeholders)

---

## Next Steps (React Native)

The scoring engine (`generatePoints`), data model (`sightings[]`), and achievements array are all self-contained and ready to extract into a React Native project. The D3 map would be replaced with `react-native-maps`.
