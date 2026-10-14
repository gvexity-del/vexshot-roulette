VEXSHOT ROULETTE - installable app files
=========================================

Files
  index.html            the game
  manifest.webmanifest  app name, colours and icons
  sw.js                 service worker (offline support)
  icons/                app icons made from the logo

How to put it online (any static host works)
  1. Upload ALL of these files, keeping the icons folder, to the same folder on an
     HTTPS host: Netlify Drop, GitHub Pages, Cloudflare Pages, etc.
  2. Open the address on your phone.
       Android (Chrome): menu > Install app (or Add to Home screen)
       iPhone (Safari):  Share button > Add to Home Screen
  3. Launch it from the new icon. It opens full screen and works offline after the first visit.

Updating the game
  After you change index.html, edit CACHE_VERSION in sw.js (for example 'vexshot-v2') and
  upload both files. Players pick up the new version the next time they open the app.

Testing on a computer
  Service workers only run on https or localhost. From this folder run:
      python3 -m http.server 8000
  then open http://localhost:8000
