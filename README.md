# Mera Mart – Affiliate Shopping Site

Static website (no server needed). Files:
- `index.html` – poori site (design + settings)
- `logo.svg` – Mera Mart logo (favicon bhi yahi hai)
- `images/` – apni carousel/product images yahan rakho (optional)

## 1. GitHub Pages par free host karna
1. github.com par account banao, **New repository** → naam e.g. `meramart` → Public → Create.
2. **Add file → Upload files** → `index.html`, `logo.svg`, `README.md` (aur `images/` folder) drag karo → **Commit changes**.
3. Repo → **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main`, folder `/ (root)` → Save.
4. 1-2 minute baad site live: `https://<aapka-username>.github.io/meramart/`
   - Agar repo ka naam `<username>.github.io` rakho to link sirf `https://<username>.github.io/` hoga.
5. Custom domain (`.com`) free nahi hota; github.io address free hai.

## 2. Pehle yeh settings badlo (`index.html` ke upar `SITE`, `MERCHANTS`)
- Amazon: `MERCHANTS.amazon.tag` me apna Associates tracking ID (e.g. `meramart-21`).
- Flipkart / Myntra / Meesho: approved affiliate link Sheet ke `aff_link` column me daalo.
- `SITE.contactEmail` aur `SITE.privacyUrl` bharo (footer me tabhi dikhenge).

## 3. Carousel (10 slides)
`SLIDES` me 10 slides hain. Apni product image lagane ke liye:
1. Image ko repo ke `images/` folder me upload karo (e.g. `images/phone.png`; transparent PNG sabse achhi lagti hai).
2. Us slide me `img:"images/phone.png"` likho.
Khali chhodoge to emoji-illustration dikhega. Sirf wahi images lagao jinke rights aapke paas hain (Amazon/Flipkart ki images copy mat karo; unki terms ke hisab se hi use karo).

## 4. Live products (Google Sheet)
Row 1 headers exactly:
`id | category | title | description | merchant | url | aff_link | emoji | image | price | old_price | deal`
- `category` menu ke naam jaisa hi (e.g. `Electronics`).
- `merchant`: `amazon`, `flipkart`, `myntra`, `meesho`.
- `image`: `images/xyz.jpg` ya https image link (khali = emoji).
- `deal`: `yes` likho to Today's Deals me bhi aayega.
- Sheet → File → Share → **Publish to web** → CSV → link ko `SITE.sheetCsvUrl` me paste karo.
- Har category me max 15 products dikhte hain.

## 5. Colors
Amazon-style navy (`#131921`) + orange/yellow aur Flipkart-style blue (`#2874f0`) + yellow: `:root` me variables badal sakte ho.

## 6. Compliance
Disclosure visible rakho, Amazon Associates aur networks ke rules follow karo, click tracking ON karo to privacy page banao.
Published Google Sheet public hoti hai: usme secret mat rakho.
