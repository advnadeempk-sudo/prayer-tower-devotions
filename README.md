# Prayer Tower Daily Devotions

Public feed of the daily devotional published on **https://prayertower.church** by
**Pastor NADEEM SALEEM M.A, M.div, LLB (Hons), LLM (HR)**, Revival Church International.

- `devotions/index.json` — the machine-readable feed the tower reads every morning
- `devotions/YYYY-MM-DD-slug.md` — the readable archive of each devotion

## How the daily cycle works

| Time (PKT) | What happens | Who |
| --- | --- | --- |
| 06:00 | Claude's scheduled task writes the new devotion into this repository | Claude |
| 06:20 | The tower's `devotion-sync` function reads `index.json`, publishes the devotion and sets it as **Today's devotion** on the home page | Netlify |
| 06:21 | The devotion is live at `prayertower.church/devotions/<slug>` and listed in the sitemap for Google | — |

To stop or edit a devotion: unpublish it from the Pastor's desk on the tower, or edit the entry here before 06:20.

## Devotion standard (editorial)

1. **Keyword-led topic.** Each devotion is built around one search phrase people actually type (focus keyword) — e.g. *prayer for healing*, *how to pray for my family*, *Bible verses about anxiety*, *morning prayer*, *prayer for Pakistan*. The focus keyword appears in the title, first paragraph, meta title and meta description, naturally.
2. **Scripture first.** One main passage (KJV quoted; other versions paraphrased), reference stated at the top.
3. **One truth, one Greek/Hebrew word.** A single clear teaching, with one original-language word explained in plain English.
4. **Life, then application.** A short story or example, then "how to live it today".
5. **The tower connection.** One paragraph linking the truth to 24-hour prayer, the persecuted church, or praying for the nations — never forced.
6. **Closing prayer** the reader can pray aloud (≤ 700 characters).
7. **Pray with us today** — three bullet points, one always for persecuted believers.
8. **Length:** 350–600 words (body ≤ 3,500 characters). Short paragraphs; reads well on a phone.
9. **Signature line, always exact:** `Pastor NADEEM SALEEM M.A, M.div, LLB (Hons), LLM (HR)`
10. **Sources.** Pastor Nadeem's own sermons and notes in Google Drive are primary; recognised public-domain and openly available commentaries, lexicons and sermons enrich them. Never name third-party books or authors in the text; never copy more than a short phrase from any copyrighted source.
11. **Safety.** Nothing attacking any person, community or faith; nothing about sacred figures of other religions or public officials; no names of believers in hostile contexts.

## SEO package (per devotion, stored in `seo`)

- `metaTitle` ≤ 60 characters, keyword first, ends "| Daily Devotional – Prayer Tower"
- `metaDescription` 140–155 characters, contains the keyword and a call to pray
- `focusKeyword` + 6–8 `keywords` (long-tail: "prayer for…", "how to pray…", "Bible verses about…")
- `tags` (3–5) for the devotions index
- `slug` lower-case, hyphenated, keyword-based, no dates

## Topic calendar (rotates; no repeat within 90 days)

Mon: Prayer & intercession · Tue: Faith & trust · Wed: Healing & comfort · Thu: Family & marriage ·
Fri: Perseverance & spiritual warfare · Sat: Persecuted church & nations · Sun: Worship, revival & the Word.
Christian calendar dates (Advent, Lent, Easter, Pentecost) and days of national prayer take priority.
