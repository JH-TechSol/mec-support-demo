# MEC Global Support Desk — proposal & demo

Self-contained web pages for the ASI / MEC support-desk proposal. No install, no login, no build step.

**Contents**
- `index.html` — landing page linking the two below
- `proposal.html` — the one-page written proposal
- `demo.html` — the interactive click-through demo (Dublin / Dubai)
- `CNAME` — custom-domain file for GitHub Pages (edit before use)

---

## Option A — just send it (easiest for Andy)

Zip this folder and email it. Andy unzips and **double-clicks `index.html`** — it opens in his browser and runs offline. Nothing to install. (With no internet the fonts fall back to system fonts; everything still works.)

Best in Chrome, Edge or Safari.

---

## Option B — host it on GitHub Pages (a clean link to send)

1. On github.com, create a new repository, e.g. `mec-support-demo`.
2. Upload these four files (drag-and-drop in the repo's web UI, or `git push`).
3. In the repo: **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**; set branch to **main** and folder to **/ (root)**; **Save**.
5. Wait ~1 minute. The site goes live at:
   `https://<your-github-username>.github.io/mec-support-demo/`
6. Send Andy that link.

---

## Option C — put it on the JH Technical Solutions domain

Use a subdomain (simplest) — e.g. `demo.jhtechnicalsolutions.com`:

1. Edit the `CNAME` file so it contains only your chosen domain, on one line:
   `demo.jhtechnicalsolutions.com`
2. In the repo: **Settings → Pages → Custom domain**, enter the same domain, **Save**.
3. At your domain registrar / DNS host, add a **CNAME record**:
   - **Host / Name:** `demo`
   - **Value / Target:** `<your-github-username>.github.io`
4. Back in **Settings → Pages**, wait for the check to pass, then tick **Enforce HTTPS**.
5. Live at `https://demo.jhtechnicalsolutions.com`.

*(For the root domain — `jhtechnicalsolutions.com` with no subdomain — GitHub Pages needs A records instead of a CNAME. See GitHub's "Managing a custom domain" docs for the current apex IP addresses. A subdomain is cleaner and won't touch your main site.)*

---

## Privacy note

GitHub Pages sites (Options B and C) are **public** — anyone with the link can open them, and the repo is discoverable unless set private (private-repo Pages needs a paid GitHub plan). The demo contains only sample data, no client-confidential material. If you'd rather keep it fully private, **Option A** (email the file) hosts nothing publicly. Netlify or Cloudflare Pages are alternatives if you want a hosted link with password protection.
