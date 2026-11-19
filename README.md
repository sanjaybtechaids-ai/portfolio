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

### Certificate URLs

Each certificate is created with three independent, editable properties:

- `imageSrc`: replace `PASTE_CERTIFICATE_IMAGE_URL_HERE` with a publicly available image URL.
- `documentUrl`: replace `PASTE_CERTIFICATE_PDF_URL_HERE` with a publicly available PDF URL.
- `verificationUrl`: replace `PASTE_VERIFICATION_URL_HERE` only when a known verification URL is available.

The UI deliberately shows a polished placeholder when an image has not been supplied, disables the PDF action when no PDF is present, and hides verification when no verification URL is present.

## Resume

Put the real resume at `public/resume/Sanjay_S_Resume.pdf`. The UI detects when this file is missing and disables resume actions instead of linking to a broken file.

## Contact form

The form validates its fields and includes a honeypot. It intentionally does not pretend to send messages without a configured endpoint. Before the main script executes, set a public endpoint in a separate local configuration script:

```html
<script>window.PORTFOLIO_CONTACT_ENDPOINT = "https://your-service.example/contact";</script>
```

That endpoint should validate requests and keep any email-provider secrets on the server—never in browser JavaScript.

## Personal links

Replace these placeholders in `index.html` with real values:

- `YOUR_EMAIL_HERE`
- `YOUR_GITHUB_URL_HERE`
- `YOUR_LINKEDIN_URL_HERE`

## Deploy

This is a static site and can be deployed by uploading the project to GitHub Pages, Netlify, Vercel, or Cloudflare Pages. Configure the publish directory as the project root; no build command is needed.
