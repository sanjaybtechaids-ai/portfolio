# Sanjay S Portfolio

A dependency-free, responsive static portfolio built with HTML, CSS, and JavaScript.

## Run locally

Open `index.html` in a browser, or serve this directory with any static-file server. For example:

```powershell
python -m http.server 4173
```

Then visit `http://localhost:4173`.

## Edit portfolio data

All skills, projects, timeline entries, achievements, and certificates live in `script.js`.

### Project URLs and screenshots

Each project entry in `script.js` can include an `imageUrl` for its preview image and a `liveLink` for its deployed demo. Both are displayed automatically when provided.

### Certificate URLs

Each certificate is created with three independent, editable properties:

- `imageSrc`: replace `PASTE_CERTIFICATE_IMAGE_URL_HERE` with a publicly available image URL.
- `documentUrl`: replace `PASTE_CERTIFICATE_PDF_URL_HERE` with a publicly available PDF URL.
- `verificationUrl`: replace `PASTE_VERIFICATION_URL_HERE` only when a known verification URL is available.

The UI deliberately shows a polished placeholder when an image has not been supplied, disables the PDF action when no PDF is present, and hides verification when no verification URL is present.

## Resume

Resume actions use the public Google Drive link configured in `index.html`. The download buttons use Drive's direct-download endpoint, and the view button opens the share page in a new tab.

## Contact form

The static-site contact form uses Formspree's vanilla JavaScript integration with the configured form ID `xrpqandq`. It includes native fallback submission, validation state, a submit-state button, and a spam honeypot. No server code, secret, or local endpoint configuration is required.

## Personal links

Replace these placeholders in `index.html` with real values:

- `YOUR_EMAIL_HERE`
- `YOUR_GITHUB_URL_HERE`
- `YOUR_LINKEDIN_URL_HERE`

## Deploy

This is a static site and can be deployed by uploading the project to GitHub Pages, Netlify, Vercel, or Cloudflare Pages. Configure the publish directory as the project root; no build command is needed.
