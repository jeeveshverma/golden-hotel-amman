# Golden Hotel Amman: website

A static website (HTML, CSS and a little JavaScript) in English (`/`) and Arabic (`/ar/`).
It needs no build step, no server code and no database. Bookings go straight to WhatsApp (+962 7 9980 1610) with a pre-filled message.

## Files

```
index.html            English home page
ar/index.html         Arabic home page (right to left)
404.html              "Page not found" page
assets/css/style.css  All styles
assets/css/fonts.css  Self-hosted fonts (no Google requests)
assets/js/main.js     WhatsApp booking form, mobile menu, animations
assets/img/           Logo (mark-gold.svg, mark-cream.svg), favicon, skyline, map, marble texture, social image
assets/img/photos/    Hotel photos, colour-corrected and resized
robots.txt, sitemap.xml, .nojekyll
```

## Preview locally

Open `index.html` in a browser. To test the way it will run online, start a local web server:

```
python3 -m http.server 8000   # then open http://localhost:8000
```

## Publish (GitHub Pages, free)

1. Create a new repository and upload everything in this folder.
2. Go to Settings → Pages → Deploy from branch → `main` / root.
3. Under Custom domain, add the domain. Then point the domain's DNS at GitHub Pages:
   four A records (185.199.108.153, .109.153, .110.153, .111.153) plus a `www` CNAME to `<user>.github.io`.

Netlify and Cloudflare Pages also work: drag and drop the folder.

## Before going live: confirm with the hotel

| Item | Current value on the site | Source |
|---|---|---|
| Domain | `www.goldenhotelamman.com` (in canonical, og, sitemap, robots) | placeholder: replace with the real domain |
| Prices | Double/Twin from $46, Junior Studio Suite from $70, Single and Junior Suite "Ask us" | Expedia, 12–14 Oct 2026, before taxes |
| Rooms | 24 | owner (listings show 23 or 35) |
| Check-in / out | 2:00 pm – midnight / before 11:30 am | Expedia |
| Payment | "Pay at the hotel", cash recommended | Expedia says cash only, Hostelworld lists cards |
| Cancellation | "We'll explain the terms on WhatsApp" | not published anywhere |
| Spa and sauna | charged separately | Trip.com / Expedia |
| Sister hotel in Petra | "Going to Petra?" card (no name or link) | owner |
| Junior Suite photo | room with a wall TV and twin beds | best match; swap if wrong |
| Email | not shown | add one if the hotel wants it |

## Editing

* **Prices:** search both HTML files for `$46` / `$70`, and update the `<option>` labels in the booking form.
* **WhatsApp number:** change `PHONE` in `assets/js/main.js` and the `wa.me/962799801610` links.
* **Photos:** replace files in `assets/img/photos/` with the same names. Better daylight photos will improve the site most.
* **Reviews:** these are verbatim quotes from verified Expedia reviews. Keep the attribution if you change them.

Fonts: Cormorant Garamond, Manrope, Tajawal and Noto Kufi Arabic, all under the SIL Open Font License.
