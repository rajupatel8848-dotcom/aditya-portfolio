# Aditya Patel — Portfolio

A static site: plain HTML, CSS and JavaScript, with a Three.js hero loaded from a CDN (needs internet).

## Run locally
- **VS Code:** install the "Live Server" extension, right-click `index.html` -> "Open with Live Server".
- **Terminal:** `npm run dev` (uses `npx serve`) and open the printed address.
Do not just double-click `index.html` in some browsers; use a local server.

## Folder map
- `index.html` — all page sections and content
- `css/styles.css` — all styling (colours are near the top, in `:root`)
- `js/loader.js` — name loading screen (2.5 s)
- `js/main.js` — navigation, scroll animations, headings, counters, contact form
- `js/hero3d.js` — Three.js sphere, rocky floor and reflection
- `js/journey.js` — 3D disc gallery in the Journey section
- `js/clock.js` — live Jabalpur time in the hero
- `assets/images/` — portrait, logo, project images, hero render
- `assets/fonts/` — put ST Remona Neue here

## Things to edit
- **Project links and GitHub/LinkedIn/résumé:** search `index.html` for "to be added" and replace each `href="#contact"` with the real URL.
- **Project screenshots:** replace the files in `assets/images/` (keep names) or edit the `<img src>`. The Tuition Dashboard card is a drawn concept preview; swap in a real screenshot.
- **Font:** see the comment at the top of `css/styles.css`.
- **Skills:** edit the lists in the `#skills` section.

## Contact form
The form currently opens the visitor's email app (`mailto:`); nothing is sent from the page. For real submissions use a form service, for example Formspree: create a form, then in `js/main.js` replace the `location.href='mailto:...` line with a `fetch('https://formspree.io/f/YOUR_ID',{method:'POST',headers:{'Accept':'application/json'},body:new FormData(...)})` call and show success only when the response is OK.

## Deploy
Drag the whole folder into Netlify, or push it to GitHub and import it in Vercel (framework preset: "Other", no build command).

## Not included
This is not a Next.js/TypeScript project. If you want that version, ask for a conversion.
