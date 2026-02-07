## Growhive Media – Single‑Page Site

This project is a single‑page marketing site for **Growhive Media**, built with plain **HTML, CSS and vanilla JavaScript**. It includes:

- Hero section with clear value proposition
- Services, portfolio, testimonials, and “Let’s work together” contact area
- Small AI‑style chat box that answers questions about your company and encourages visitors to leave their details
- Contact form + chat callback form wired to **Formspree**

### 1. Project structure

- `index.html` – main page (all markup, styles, and scripts)
- `assets/gallery/` – images, video (`0130.mp4`), favicon, company profile PDF

### 2. Running locally

You can simply open `index.html` in a browser, but it’s better to serve it from a local web server so links and video behave like they will in production.

From the project root (`e:\Project\GROWHIVE MEDIA`):

```bash
python -m http.server 8000
```

Then open `http://localhost:8000` in your browser.

### 3. Recommended free hosting options

Because this is a static site (HTML/CSS/JS only), you can use any static hosting. Good free options:

- **Netlify** (recommended)
  - Very simple drag‑and‑drop deploy, or connect to GitHub
  - Free HTTPS, custom domain support, form handling if you ever want to move off Formspree
- **Vercel**
  - Great for static sites, automatic deploys from GitHub
  - Free HTTPS, easy custom domain setup
- **GitHub Pages**
  - Host directly from a GitHub repo
  - Good if you’re already using GitHub and don’t need form extras

For the easiest experience, use **Netlify**.

#### Deploying to Netlify (drag‑and‑drop)

1. Go to `https://app.netlify.com/` and create an account.
2. Click **“Add new site” → “Deploy manually”**.
3. Drag the entire project folder (`GROWHIVE MEDIA`) into the upload area, or zip it and upload.
4. Netlify will build and give you a live URL like `https://your-site-name.netlify.app`.
5. (Optional) Add a custom domain under **Domain settings**.

### 4. Forms & chat backend

- Both the **main contact form** and the **chat callback form** post to **Formspree** using a shared form ID.
- Update the Formspree ID in `index.html` if you change your Formspree form.
- After a successful chat callback submit, the bot responds: *“Thank you! Our sales team will email you with a quotation.”*

### 5. Customizing

- **Images & company profile**
  - Replace images in `assets/gallery/` but keep the same filenames, or update the paths in `index.html`.
  - The company profile links point to `assets/gallery/Company Profile.pdf`.
- **Favicon**
  - The browser tab icon uses `assets/gallery/favicon-32x32.png`. Replace this file to change the icon.
- **Chat behaviour**
  - All chat logic is in the `<script>` block at the bottom of `index.html` (look for `aiResponses` and `getReply`). You can edit responses or add new ones there.

