# iTabs This Talk

Talk notes you can download or paste straight into your own AI. Planned home: **talk.itabs.co**.

> **For now, talk pages live on the iTabs This Video Worker**, at `itabs-this-video.jgwynne7.workers.dev/talk/<name>` (e.g. [Aidan's page](https://itabs-this-video.jgwynne7.workers.dev/talk/aidan)). The skill in `skill/SKILL.md` points speakers, and their QR codes, at that address. **We'll switch to talk.itabs.co later.** When we do:
> 1. Connect this repo to Cloudflare Pages and add the `talk.itabs.co` domain (see `CLOUDFLARE-SETUP.md`).
> 2. In `skill/SKILL.md`, change the address back to `talk.itabs.co/<slug>`, remove the "Address for now" note, and set the page template's links back to this repo's style (as in `aidan/index.html`: relative file links and `/skill/SKILL.md`).
> 3. Copy each talk folder from the Worker's `src/talk/` into this repo.
> 4. Speakers' QR codes already printed point at the Worker, so keep the Worker's `/talk/<name>` pages running, or redirect them to talk.itabs.co.

| Talk | Page |
|------|------|
| Quality gates for agents: Make bad code fail · Aidan Morgan, Bankwest | [itabs-this-video.jgwynne7.workers.dev/talk/aidan](https://itabs-this-video.jgwynne7.workers.dev/talk/aidan) |

Plain static HTML, no build step, no logins. This repo will be hosted on Cloudflare Pages at talk.itabs.co; see `CLOUDFLARE-SETUP.md`. Until then it's the master copy of the skill and the planned talk.itabs.co site.

## Adding a talk

Speakers use the **iTabs This Talk skill** (`skill/SKILL.md`, downloadable from the "Make your own" button on every page, at itabs-this-video.jgwynne7.workers.dev/talk/skill). They add it to Claude and say "make my talk page". Claude writes the talk MD, makes a `<slug>/` folder, and makes a QR code for their last slide. They send the folder to Jon.

**For now:** Jon adds the folder to the itabs-this-video repo at `src/talk/<slug>/`, registers its files in `src/talk/talk.js`, runs `npm test` and pushes. It goes live at `itabs-this-video.jgwynne7.workers.dev/talk/<slug>`.

**When the skill changes:** edit `skill/SKILL.md` here, then copy it to `src/talk/skill/SKILL.md` in itabs-this-video and push, so the Make your own button gives the new version.

Made with iTabs · Jon · 0421 508 009 · jgwynne7@gmail.com
