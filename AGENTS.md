# AGENTS.md — jonathanmccallum-am (Amharic mirror of jonathanmccallum.com)

Amharic mirror site. Same theme and design as the main site (Paper Light),
content translated into Amharic, meaning-first. Repo: streamjonathan/jonathanmccallum-am.
Live (when approved): am.jonathanmccallum.com. Proof: jonathanmccallum-am.pages.dev.

## Mission

Mirror jonathanmccallum.com in Amharic — every article translated for meaning,
not word for word, in Jonathan's voice: plain short sentences, friendly, positive,
never preachy. An average person interested in Jesus, not an expert or theologian.

## Roles

- **Bobby (Muse) is the lead builder.** He coordinates, builds, pushes to GitHub
  and deploys to Cloudflare. He is the ONLY one who pushes or deploys.
- **Claude advises and reviews** translation quality. He does not push or deploy.
- **Helper Muses translate** one article at a time, drafts only.

## The one rule above all

**Never publish or alter live production assets without Jonathan's clear
permission.** The Amharic site goes live on am.jonathanmccallum.com only when
he says so, after reading the pilot article(s). Drafts stay drafts until he
approves them. Work on a branch, never straight on main. Give Bobby a preview URL.

## Translation rules

- English repo (streamjonathan.github.io) is the source of truth. Articles are
  translated from the English Markdown, keeping the same date, slug, source_video
  and shareImage. Only the title and body are translated.
- Register: plain, warm, honest; short sentences; no preaching. Direct address
  uses አንተ (familiar singular "you") throughout — Jonathan to confirm vs formal
  እርስዎ, which would change imperatives and possessives everywhere. Script: Ge'ez
  (ፊደል). God = እግዚአብሔር, Jesus = ኢየሱስ.
- Names (never vary): አስላን, ናርኒያ, ሉሲ, ዲጎሪ, ቲሪያን, አዳምና ሄዋን (Amharic Bible
  forms), ጴጥሮስ, ካይር ፓራቬል, ነጭ ጠንቋይ. Book titles stay in English — no
  published Amharic translation of the Narnia books was found; if one exists,
  titles should switch to it. "Surfer" stays the loanword ሰርፈር (flagged).
- Bible verses: none of the 5 articles contains a direct Bible quotation, so no
  verse text was reproduced. The bread/water of life lines are Jonathan's
  paraphrase (echoing John 6:35 / 4:14) — የሕይወት እንጀራ / የሕይወት ውኃ — never
  presented as quoted Scripture. Exact Amharic Bible wording was NOT verified;
  check against the printed Amharic Bible before quoting any verse directly.
- No direct Lewis quotations appear either; none were invented.
- No emojis, no newsletter form, no links the English article does not have.
- Never invent facts, dates, links or details.

## Site facts

- Eleventy 3, Cloudflare Pages, Paper Light theme (Fraunces + Newsreader).
- No Ask chat and no note Worker on this site yet — search (Pagefind) works,
  Ask and notes come later. The Ask floating button and ask.js are removed.
- CSS is preloaded, not inlined (CSP blocks inline style). Bump the `?v=` query
  on any CSS/JS file you change.
