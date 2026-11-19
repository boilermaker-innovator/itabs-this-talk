# Put talk.itabs.co on Cloudflare

This repo is the whole site. Plain files, no build step.

## A. Create the site (Cloudflare Pages)
1. Log in at dash.cloudflare.com → **Workers & Pages** → **Create** → **Pages** tab.
2. Choose **Connect to Git** → pick `boilermaker-innovator/itabs-this-talk`.
3. Settings:
   - Project name: `talk-itabs`
   - Production branch: `main`
   - Framework preset: **None**
   - Build command: *(leave empty)*
   - Build output directory: leave empty (or `/` if it insists)
4. **Save and Deploy**. You get a test address like `talk-itabs.pages.dev`.
   Check `https://talk-itabs.pages.dev/aidan` and try all three buttons.

   *No Git? Use **Upload assets** instead and drag in this repo's files.*

## B. Point talk.itabs.co at it
5. In the `talk-itabs` Pages project → **Custom domains** → **Set up a custom domain**.
6. Type `talk.itabs.co` → **Continue**.
7. Then one of:
   - **itabs.co's DNS is already on Cloudflare:** click **Activate domain**. Cloudflare adds the DNS record for you. Done.
   - **itabs.co's DNS is elsewhere (e.g. GoDaddy, Crazy Domains):** log in there and add a record:
     `Type: CNAME · Name: talk · Value: talk-itabs.pages.dev`. Then come back and click **Check DNS**.
8. Wait for the status to say **Active** (usually minutes, can be up to a day). HTTPS is automatic.
9. Open `https://talk.itabs.co/aidan` on your phone, and scan the QR code to test it.

## Adding the next talk
Speakers make their folder with the iTabs This Talk skill (`skill/SKILL.md`). Drop their folder (e.g. `sarah/`) in the repo root, add it to `README.md` and `index.html`, and push. It goes live at `talk.itabs.co/sarah`.
