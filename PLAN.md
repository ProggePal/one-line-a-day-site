# Website Agent Plan — One Line a Day

> Working directory: `/Users/pal/dev_pals/one-line-a-day-ios/website`
> Hosted on GitHub Pages. Zero build step, pure static HTML/CSS.
> Update STATUS section after each work session.

---

## Session Prompt

Paste this into a new Claude Code session opened in `/Users/pal/dev_pals/one-line-a-day-ios/website`:

```
Build the static website for "One Line a Day" iOS app. Hosted on GitHub Pages — zero build step, pure HTML + CSS + minimal vanilla JS.

PAGES TO BUILD:
1. index.html         — Landing page (main marketing)
2. privacy.html       — Privacy policy (required for App Store)
3. support.html       — Support page (required for App Store)

BRAND:
- Name: One Line a Day
- Tagline: "Make every day count."
- Sub-tagline: "One thought. One minute. Every day."
- Color palette: off-white (#FAF9F6), near-black (#1A1A1A), warm accent (#C97D4E)
- Font: system-ui stack (no Google Fonts, loads instant)
- Tone: calm, minimal, intentional — not a productivity hustle app

LANDING PAGE sections:
1. Hero: App name + tagline + App Store badge (placeholder link first, update later)
2. What is it: 3 short lines explaining the concept
3. Features grid (4 items): Write daily / Never lose it (iCloud) / Track your habit / Your words, your export
4. Screenshots: placeholder div with phone mockup outline (CSS only, no images needed for launch)
5. Pricing: Free + "Voice transcription: one-time $2.99"
6. Footer: Privacy / Support / © 2026

PRIVACY PAGE:
- Use Gemini to generate it: gemini -p "Write a complete privacy policy for an iOS journaling app called 'One Line a Day'. The app stores journal entries locally and syncs via iCloud. It optionally uses Apple's Speech Recognition framework for voice-to-text. No third-party analytics, no advertising, no data sold. Developer contact: [EMAIL PLACEHOLDER]. GDPR and CCPA compliant." --output-format json | jq -r '.response'
- Wrap the Gemini output in the same HTML shell as index.html

SUPPORT PAGE:
- Simple FAQ: How to export? / How to delete data? / How does iCloud sync work? / How to restore purchase?
- Contact email: [EMAIL PLACEHOLDER]
- Link back to landing page

GITHUB PAGES SETUP:
- All files in /website root
- Create CNAME file if custom domain wanted (leave blank for now)
- Create .nojekyll file to skip Jekyll processing

Use Gemini headless for copy generation:
  gemini -p "PROMPT" --output-format json | jq -r '.response'

IMPORTANT: The privacy policy URL must be live before App Store submission.
After building, write CHECKPOINT.md with the GitHub Pages URL and status.
```

---

## Task Checklist

- [ ] `index.html` — landing page
- [ ] `privacy.html` — privacy policy
- [ ] `support.html` — support/FAQ
- [ ] `.nojekyll` — GitHub Pages config
- [ ] CSS is inline or single `style.css` (no build)
- [ ] Mobile responsive
- [ ] App Store badge link (placeholder ok)
- [ ] All pages link to each other
- [ ] Pushed to GitHub → Pages enabled
- [ ] Privacy policy URL confirmed live

---

## Status

**Current phase:** Not started
**Last worked on:** —
**GitHub repo:** — (create: `one-line-a-day-site` or use a `/docs` folder)
**Live URL:** —
**Notes:** Privacy page must be live before App Store submission.
