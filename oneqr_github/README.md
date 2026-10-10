# OneQR — Interactive Website Prototype

A responsive static landing page for the OneQR universal merchant action-layer concept. Built with plain HTML, CSS, and JavaScript; no build step or package manager is required.

## Run locally

Open `index.html` in a modern browser.

## Publish using GitHub Pages

1. Create a new repository on GitHub (for example, `oneqr-website`).
2. Upload `index.html`, `README.md`, and `.nojekyll` to the repository's **root** directory.
3. Commit the files to the `main` branch.
4. Open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select branch `main` and folder `/(root)`, then click **Save**.
7. Wait for the Pages deployment to finish. The site URL will be shown in **Settings → Pages**.

For a project repository named `oneqr-website`, the URL is typically:
`https://YOUR-USERNAME.github.io/oneqr-website/`

For a repository named `YOUR-USERNAME.github.io`, the URL is typically:
`https://YOUR-USERNAME.github.io/`

## Prototype limitations

- The QR visuals in this prototype are decorative; they are not scannable QR codes.
- The early-access form is client-side only; it does not store or send submissions.
- No backend, authentication, merchant dashboard, booking/order persistence, or real payment integration is connected.
- Prices shown are hypotheses for market testing, not live offers.
- Do not enter real customer or payment information into this demo.

## Next development milestone

Build the real merchant onboarding and setup dashboard, then generate a scannable QR for each published merchant page. Add persistent storage and authentication only after the user flows have been validated.
