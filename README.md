# CalPak — Pakistani Calorie Tracker

A beautiful, offline-first PWA (Progressive Web App) for tracking daily calories with 100+ Pakistani foods pre-loaded.

## Features 🎯

✅ **100+ Pakistani Foods Pre-loaded**
- Roti, Naan, Biryani, Pulao, Daal, Karahi, Kebab, etc.
- Fruits, Vegetables, Dairy, Drinks, Snacks

✅ **Core Functionality**
- Daily calorie tracking with visual ring progress
- Portion size adjustment (grams, pieces, servings, cups, tbsp)
- Macros tracking (Carbs, Protein, Fat)
- Customizable daily goal (1500-3000+ kcal)
- Water intake tracker (8 glasses)
- 30-day history with trends

✅ **User Features**
- Google Sign-In (via Firebase)
- Demo mode (no login required)
- Local data storage (secure on your device)
- Export to CSV
- Clear/edit entries

✅ **Tech Features**
- 100% Offline capable (works without internet)
- Installable on Android home screen
- Works on iOS, Android, Desktop, Tablet
- Zero server required for basic use
- Responsive design

## Deploy in 5 Minutes

### Option 1: Free Hosting (Vercel, Netlify)

**Vercel** (recommended for beginners):
1. Go to https://vercel.com
2. Click "Import Project" → "Git Repository"
3. Upload this folder, confirm, deploy
4. Your app is live at `your-project.vercel.app`

**Netlify**:
1. Go to https://netlify.com
2. Drag & drop this folder onto "Sites"
3. Done!

### Option 2: GitHub Pages

```bash
# Push to GitHub
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/calpak
git push -u origin main

# Go to repo → Settings → Pages → Deploy from main branch
# Your app is live at YOUR_USERNAME.github.io/calpak
```

### Option 3: Your Own Server (nginx, Apache)

Just upload these 3 files to your web server:
- `index.html`
- `sw.js`
- `manifest.json`

Make sure they're served with correct MIME types:
- `.html` → `text/html`
- `.json` → `application/json`
- `.js` → `application/javascript`

## Setup Google Sign-In (Optional)

To enable Google Login instead of demo mode:

1. Go to [Firebase Console](https://console.firebase.google.com)
2. Create a new project (name: "CalPak")
3. Go to **Authentication** → **Sign-in method** → **Google** → Enable
4. Go to **Project Settings** → **Your apps** → **Add Web App**
5. Copy these values:
   - `apiKey`
   - `authDomain`
   - `projectId`
6. When you first open CalPak, paste them in the Firebase modal
7. Config is saved locally on your device

## Install on Android

1. Open CalPak in Chrome
2. Tap ⋮ (menu) → "Install app"
3. Tap "Install"
4. CalPak appears on your home screen

Or from the app itself:
- The orange banner appears automatically
- Tap "Install" to add to home screen

## File Structure

```
calpak/
├── index.html        ← Main app (all UI + logic)
├── sw.js             ← Service Worker (offline cache)
├── manifest.json     ← PWA metadata
└── README.md         ← This file
```

That's it! No build step, no npm, no backend.

## Features Coming Soon 🚀

- 📱 Barcode scanner (for packaged foods)
- 🍽️ Meal planning & saved meals
- 👥 Family sharing
- 📈 Weekly/monthly analytics
- 🔔 Notifications & reminders
- 🍳 Recipe database (Pakistani recipes)
- 🌙 Dark mode
- 🇵🇰 Urdu language support

## Customization

### Add More Foods

Edit the `FOOD_DB` array in `index.html` (around line 380):

```javascript
{id:'xyz', name:'Samosa', emoji:'🔺', cat:'Snacks & Street Food', cal:130, carbs:15, protein:3, fat:7, unit:'piece', basis:'piece'},
```

Macros guide:
- **Carbs** = grams of carbohydrates
- **Protein** = grams of protein
- **Fat** = grams of fat

### Change Colors

Edit CSS variables at the top of `<style>`:

```css
:root {
  --green: #1a6b3c;        /* Primary color */
  --saffron: #f4a500;      /* Accent */
  --red: #e63946;          /* Error */
}
```

### Add Your Logo

Replace the "CalPak" text in the header with an image:

```html
<img src="your-logo.png" width="100" />
```

## Data Privacy

✅ All your data is stored **locally on your device**
✅ Nothing is sent to any server (unless you add Firebase)
✅ You can export anytime as CSV
✅ Data persists offline

## Browser Support

| Browser | Status |
|---------|--------|
| Chrome/Edge (Android) | ✅ Full support |
| Firefox (Android) | ✅ Full support |
| Safari (iOS) | ✅ Full support |
| Samsung Internet | ✅ Full support |
| Desktop Chrome/Firefox | ✅ Full support |

## Troubleshooting

**"Google Sign-In not working"**
- Make sure Firebase config is entered correctly
- Add your domain to Firebase → Settings → Authorized Domains
- For localhost, it's already pre-approved

**"Service Worker not registering"**
- Make sure you're on HTTPS (or localhost)
- Clear browser cache, hard refresh (Ctrl+Shift+R)
- Check DevTools → Application → Service Workers

**"Data not saving"**
- Check browser storage isn't full
- Try exporting and clearing cache
- Check if localStorage is enabled

**"Install button not showing"**
- Must be on HTTPS (except localhost)
- Must have manifest.json properly configured
- Try on Chrome Android first
- iOS: Use "Add to Home Screen" in Safari share menu

## Support & Feedback

Found a bug? Have a feature request? Add Pakistani foods?

Create an issue or email: feedback@calpak.app

---

**Made with 🇵🇰 love for Pakistan** | v1.0.0
