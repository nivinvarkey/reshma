# Adv. Reshma Raj — GitHub Pages website

## Publish portfolio
1. Create a new public GitHub repository, e.g. `reshma-portfolio`, in the account where you want to host it.
2. Upload `index.html`, `styles.css`, `script.js`, `favicon.svg`, and `Reshma_Raj_Resume.pdf` to the repository root. (`main-site-entry.json` is for your main hub, not required here.)
3. Go to repository **Settings → Pages**, select **Deploy from a branch**, `main` and `/ (root)`; save.
4. Test your `https://USERNAME.github.io/reshma-portfolio/` URL first.

## Connect the subdomain
In GoDaddy DNS for `professionals-cv.in`, create:
- Type: `CNAME`
- Name: `reshma`
- Value: `USERNAME.github.io` — replace USERNAME with the actual GitHub username that owns the new portfolio repository (no `https://`, no repo path).

Then in the portfolio repository **Settings → Pages → Custom domain**, enter `reshma.professionals-cv.in` and save. Enable Enforce HTTPS after provisioning. You may also add a root-level `CNAME` file containing exactly `reshma.professionals-cv.in`; GitHub Pages normally manages this file when saving the custom domain in branch deployment mode.

## Add to the main website
In the main hub's `sites.json`, add the object from `main-site-entry.json` inside the existing array, ensuring commas are valid. Change `"status": "coming-soon"` to `"status": "live"` only once the new URL works. Your hub may use specific icon names or status labels; align with the existing `script.js` schema.

### Important
- You should check with Reshma before publicly publishing the included résumé, mobile number and email address. Remove the résumé PDF or personal contact fields if she does not want them public.
- This is a professional portfolio, not legal advice or a claim of eligibility to practice in any new jurisdiction.
