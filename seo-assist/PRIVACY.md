# SEO Assist Privacy Policy

**Version 1.1, 22 October 2026.** SEO Assist is a browser extension made by HITAN.

## In short

SEO Assist has no account, no sign-up, no analytics and no tracking. HITAN does not receive any of your data. The extension talks only to the website you choose to audit and, if you use them, to Google PageSpeed Insights and Anthropic (Claude).

## What SEO Assist reads

- **The page you audit.** When you press Analyze, SEO Assist reads that page's content (title, headings, text, links, images, structured data) to check it against Google's SEO guidance.
- **The site you crawl.** If you start a site crawl, it fetches pages of that same site. Access to a site is asked for at the moment you audit it, one site at a time.
- **The address of the open tab**, so the side panel knows which page to audit.

## What leaves your computer, and only when you use it

| Where | What | When |
|---|---|---|
| The audited website | Normal page requests, marked "SEO Assist" in the User-Agent | When you audit or crawl it |
| Google PageSpeed Insights (www.googleapis.com) | The address of the audited page, and your PageSpeed key if you added one | When the speed check runs (can be switched off in Settings) |
| Anthropic (api.anthropic.com) | The audit results and the page details they are based on, and your own Claude key | Only when you press Explain: first to count the cost, then, after you confirm, for the suggestions |
| Google Search Console (googleapis.com), if you connect it | The address of the audited page and a read only sign in token, to read that page's clicks, searches and index status from your own Search Console | Only after you press Connect Search Console; the sign in ends when the browser closes |

Google and Anthropic handle that data under their own privacy policies:
https://policies.google.com/privacy and https://www.anthropic.com/legal/privacy.

## What is stored, and where

Everything is stored in your own browser:
- **Your API keys** (Claude, PageSpeed): on this computer only, never synced.
- **The Search Console sign in**, if you connect it: in memory for this browser session only; it is deleted when the browser closes, and Disconnect revokes it.
- **Settings and reminders:** in your browser's sync storage, so they follow your Chrome profile.
- **Audit history, crawl results and an error log** (the newest 50 errors, with anything that looks like a key removed): on this computer only.

Removing the extension deletes all of it. The error log can also be cleared in Settings.

## What SEO Assist never does

- It never sells, shares or transfers your data, and never uses it for advertising or credit decisions.
- It never reads pages you have not chosen to audit, and never changes any website.
- It never sends anything to HITAN.

## Changes and contact

If this policy changes, the version and date above change with it. Questions: HITAN, https://hitan360.com.
