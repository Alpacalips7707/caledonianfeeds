# Caledonian-Record Web Feed

This repository is the publishing bridge between ChatGPT and BLOX CMS for selected web-only content.

## Publishing rule

Nothing is added to the feed unless Todd explicitly instructs ChatGPT to publish it to the web feed.

## Files

- `web-feed.xml` — RSS 2.0 feed consumed by BLOX.
- `content/` — archive of published article records.
- `community-announcements.xml` — existing legacy feed; left untouched.

## Article record

Each published story is stored as a JSON file containing:

- `id`
- `status`
- `headline`
- `byline`
- `source`
- `categories`
- `published`
- `link`
- `body_html`

## Commands

Natural-language commands in ChatGPT are the editorial interface:

- `Publish this to the web feed` — create an article record and add it to RSS.
- `Update that feed story ...` — revise the article record and corresponding RSS item.
- `Unpublish that story` — remove it from RSS while retaining its archive record as unpublished.

BLOX remains the downstream CMS and handles section mapping, workflow and publication after import.
