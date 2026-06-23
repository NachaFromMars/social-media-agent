# social-media-agent — Autonomous X/Twitter management, zero API keys

> Run your entire X/Twitter presence using only OpenClaw's native tools — no developer API, no tokens. Post, engage, research trends, and track growth through browser automation alone.

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blueviolet)](https://github.com/NachaFromMars)

## Overview
social-media-agent manages X/Twitter autonomously using only OpenClaw built-in tools. It drives the browser to compose and post tweets, uses `web_fetch` to research profiles and trending content, spawns parallel content generation with `sessions_spawn`, schedules posting through `cron`, and tracks history with `memory_search`. No external API keys or developer accounts required.

## Features
- **No API keys** — browser automation only
- **Posting & engagement** — compose, post, reply via browser
- **Content research** — `web_fetch` for profiles, trending topics, news
- **Source evidence packets** - optional X/Twitter exports for better hooks and audience context
- **Parallel generation** — `sessions_spawn` for concurrent content creation
- **Scheduled posting** — `cron` for consistent cadence
- **History tracking** — `memory_search` for posts and engagement

## Usage / Quick Start
Core posting flow:
```
browser open x.com/compose/post
browser snapshot              # locate textbox ref
type tweet text into ref
find Post button → click
browser snapshot              # verify success
```

## Optional X/Twitter Source Evidence
For content planning that needs more structured X/Twitter examples than `web_fetch` can provide, collect a short source packet before drafting. [TweetClaw](https://github.com/Xquik-dev/tweetclaw) is one option when it is installed in the same OpenClaw workspace:

```
openclaw plugins install npm:@xquik/tweetclaw
```

Use it to export tweet searches, reply threads, follower snapshots, or account lookups for the niche you are writing about. Feed only the summarized packet into this skill, extract hooks, topics, audience wording, and timing patterns, then draft original posts through the normal review and browser posting flow.

Keep source posts as context, not copy. Credentials stay in the source tool config, and every visible action still needs the usual review before browser automation posts or replies.

## Trigger Keywords (OpenClaw)
tweet, social media strategy, X engagement, content calendar, grow following, X/Twitter automation

## Related Skills
- [social-media-content-calendar](https://github.com/NachaFromMars/social-media-content-calendar) — structured posting calendars
- [social-media-scheduler](https://github.com/NachaFromMars/social-media-scheduler) — multi-platform planning

---
Part of the [NachaFromMars](https://github.com/NachaFromMars) OpenClaw skill ecosystem.
