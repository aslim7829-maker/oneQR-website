OneQR — Stage 2 merchant setup prototype
OneQR is a responsive static website prototype for a universal merchant action page. This version adds a merchant setup dashboard and generates real scannable QR codes that open a public merchant page.
Files
`index.html` — project landing page and concept demo.
`dashboard.html` — merchant setup form, action selector, live preview, QR generation and QR PNG download.
`merchant.html` — public page opened by scanning the generated QR code.
`qr-engine.js` — local JavaScript QR-generation engine; no external QR CDN is required.
`THIRD_PARTY_NOTICES.md` and the license files — third-party source notices.
Publish/update with GitHub Pages
Download the OneQR Stage 2 ZIP and extract it on your computer.
Open your existing GitHub repository.
Upload the contents of the extracted folder into the repository root (the same folder that contains your current `index.html`). Do not upload the parent folder itself.
When GitHub reports that `index.html` or `README.md` already exists, choose to replace/overwrite those files. Add `dashboard.html`, `merchant.html`, `qr-engine.js`, `THIRD_PARTY_NOTICES.md`, `LICENSE-APACHE-2.0.txt`, and `LICENSE-MIT.txt`.
Commit the change to the same branch and folder already used in Settings → Pages (typically `main` and `/(root)`).
Wait for the Pages deployment to succeed in the repository's Actions tab, then refresh the site. If the old page appears, try a hard refresh (Ctrl+F5).
If the repository is named `oneqr-website`, URLs typically look like:
`https://YOUR-USERNAME.github.io/oneqr-website/`
`https://YOUR-USERNAME.github.io/oneqr-website/dashboard.html`
Use the actual GitHub username and exact repository name. The dashboard uses relative URLs, so it supports a project site hosted under a repository subpath.
Try the prototype
Open the live site and click Build your merchant page, or open `dashboard.html` directly.
Enter a business name, business category and only public contact details.
Enable up to six customer actions. Add a destination URL for actions such as a menu, booking form or order page where relevant.
Select Generate my QR.
Download the PNG, scan it with a phone camera, and test the public page.
A merchant draft is stored in `localStorage` on the current browser only. The public page's business profile is encoded in the QR link, so the link works on another device without a backend.
Important prototype limitations
The QR code is real and scannable, but it contains profile data inside the URL. Changing the profile changes the QR code. A stable QR that stays the same while profile details change requires a backend and a stable merchant ID/URL.
This static version has no merchant accounts, shared database, admin controls, saved customer records or centralized analytics.
Bookings, orders, repair status, estimates, warranty lookup, receipts and payments are not processed by OneQR. The business must configure a destination URL for a supported external workflow. Calls, WhatsApp links, business website links and map links can open directly where configured.
No private customer, vehicle, warranty or payment information should be placed in the public QR profile.
The project is not a bank, payment processor or official LankaQR service.
Test the QR after deployment using a second device. Do not use QR links containing sensitive information.
Recommended Stage 3
Add Supabase (or a comparable backend) with merchant authentication, a merchants table, stable public slugs, managed action settings, access policies and a publishing workflow. Then the printed QR can contain a short stable URL such as `/m/green-basket`, while the merchant updates content through the dashboard without reprinting the code.
