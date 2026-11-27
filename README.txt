ENERGY REDIRECT - INSTALLABLE APP

Upload ALL of these files, keeping the icons folder, to one folder on any HTTPS host.
GitHub Pages works:
  1. Create a new repo (for example energy-redirect).
  2. Upload index.html, manifest.webmanifest, sw.js and the icons folder.
  3. Settings > Pages > Deploy from branch: main, folder / (root). Save.
  4. Open the address GitHub shows, e.g. https://jamesonflex.github.io/energy-redirect/

Install on Android (Chrome): open the address > menu (three dots) > Install app.
Install on iPhone (Safari): open the address > Share > Add to Home Screen.

Updating: replace index.html with a new version. When you make a big change,
also change 'energy-redirect-v1' in sw.js to v2, v3... so phones refresh their saved copy.


ROOF DESIGNER (designer.html)
Rep tool for laying out solar on a real roof. Open: https://jamesonflex.github.io/energy-redirect-app/designer.html
(also linked as "Rep design tool" in the app footer).

Type an address -> pick a suggestion -> the satellite view loads at true scale, and Google's
Solar API places panels on the roof with per-panel production. Fit to 8/10/12 kW, tap panels
to block vents or skylights, then copy the proposal text.

Turn on Google (one-time, about 10 minutes):
  1. console.cloud.google.com -> create a project -> attach a billing account.
  2. APIs & Services > Library -> enable: Maps JavaScript API, Places API (New),
     Maps Static API, Solar API.
  3. APIs & Services > Credentials -> Create credentials -> API key.
  4. Restrict the key (important: the repo is public, so anyone can see the key):
       Application restrictions: Websites -> add  https://jamesonflex.github.io/*
       API restrictions: only the 4 APIs above.
  5. Either paste the key into the "Google API key" box in the designer (saved per device),
     or put it in designer.html: const GOOGLE_KEY='...'; so every device has it.
  6. Optional: set daily quota caps on each API in the Cloud console to cap spend.

No Google coverage for a house? Upload a north-up screenshot, tap Set scale on an edge you
know, and draw the roof faces by hand.
