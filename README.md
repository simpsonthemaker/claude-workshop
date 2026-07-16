# Claude Workshop Landing Page

Live page for the free "Claude Training for Real Estate Agents" workshop.
Hosted on GitHub Pages: https://simpsonthemaker.github.io/claude-workshop/

---

## Weekly workflow

One page, one session per week. Two things to do each week:

### 1. Update the date

Open `index.html`, scroll to the bottom, and edit these two lines only:

```js
const WORKSHOP_DATE_FULL  = "Wednesday, July 22 · 10:00 AM MST";  // long version
const WORKSHOP_DATE_SHORT = "Wed July 22";                        // short pill version
```

Every date on the page reads from these two lines, so there is nothing else to change. They can never disagree.

### 2. Decide how to share the link

Same page and URL every week. What changes is who gets it.

- **Team / private week:** send the link to ONE broker only. They forward it to their team. Do not post it publicly that week.
- **Mixed / open week:** share the link everywhere (YouTube, email list, socials). Anyone can sign up.

---

## Attribution (once Kit is connected)

To track which team an agent came from, add a tag to the end of the link when you share it:

- Team week: `https://simpsonthemaker.github.io/claude-workshop/?t=remax-first`
- Open week: `https://simpsonthemaker.github.io/claude-workshop/?t=open`

The tag lets you group signups by source in Kit. Agents never pick anything, the link carries it.

**Note:** tags only do something once the Kit form is connected. Until then the forms do not capture data, and "who you share the link with" is the whole mechanism.

---

## Still to do

- Connect both signup forms to Kit (ConvertKit).
- The page has two forms: the hero form (`name` / `email`) and the register card (`name2` / `email2`). Both need to map to the same Kit fields.
- Wire the `?t=` URL tag into a Kit hidden field so team attribution is captured automatically.

---

## Publishing changes

```bash
cd ~/Desktop/"October Claude Realtor OS Build"/"Workshop Desktop"/claude-workshop
git add -A
git commit -m "Describe the change"
git push origin main
```

GitHub Pages rebuilds automatically about a minute after each push.
