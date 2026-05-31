# Hi, I'm Andrew

PM at an AI company, former ClimateTech. I build side projects to stay close to the tech — and because the intersection of AI and climate is too interesting not to tinker with.

My process: plan with Claude, build with Cursor, deploy until it actually works. I went from zero idea to a deployed product in 20 hours on one of these. That still feels insane to me.

Below are my public projects. I have others that aren't.

---

## 🌍 [CarbonCoach](https://github.com/abrose1/CarbonCoach)

A conversational tool that calculates your personal carbon footprint, recommends personalized ways to reduce it, and searches 680 state and federal programs to surface financial incentives you may not know about (powered by the DSIRE database). Takes about 5 minutes and 15 messages to complete.

The thing I find interesting: each Carbon Coach conversation emits ~7.8g of CO₂. A user who installs a heat pump or solar panels based on a recommendation reduces their footprint by ~4,000,000g/year. One in every ~500,000 users following through makes the app net-positive on carbon. The math isn't as scary as you'd expect.

Built with Claude as the conversational interface. Full-stack: Flask, PostgreSQL, state-specific EPA emission factors.

`Python · Flask · Anthropic · PostgreSQL · HTML/CSS/JS`

---

## ⚡ [ProjectBurnout](https://github.com/abrose1/ProjectBurnout) + [mcp-server-eia](https://github.com/abrose1/mcp-server-eia)

Two connected projects born from the same weekend.

**Project Burnout** is a stranded asset dashboard tracking 100+ MW coal and gas plants across the U.S. Many are projected to operate at a loss for years after cheaper renewables should have replaced them — locked in by contracts, debt, and regulation. (And there are serious discussions about building *new* coal plants to power AI demand. That would be a mistake.) Burnout visualizes the gap between when each plant becomes unprofitable and when it actually shuts down, based on EIA filings and financial projections. Has a natural language query bar powered by Claude — I wanted to explore LLMs outside the chat interface, and I've found it genuinely useful.

**mcp-server-eia** started as practice building MCPs. The dashboard didn't end up needing one, so I built it anyway as a standalone tool. It's not a thin API wrapper — it's 10 domain-aware tools for querying plant inventory, generation mix, fuel prices, AEO projections, and state CO₂ emissions in a shape AI agents can actually use reliably. Free to use if you're building AI tools for energy or climate.

`Python · FastAPI · React · Anthropic · EIA API · MCP · Postgres`

---

## 📬 [ReleaseWatcherAgent](https://github.com/abrose1/release-watcher)

A scheduled agent that monitors new releases across books, music, TV, and film — and texts me when something worth paying attention to comes out. Runs on Railway Cron, polls Spotify, TMDB, Google Books, and Brave Search, then uses Claude to judge whether a release actually fits my taste before firing a Twilio SMS.

It reads from a private **taste-profile** repo that ingests my ranked bookshelves and Spotify history to score authors and artists into tiers. That repo isn't public (it has personal taste data in it), but the release-watcher README covers how the two-repo architecture works if you want to adapt it.

This one's purely for me — but it was a good excuse to build something with real multi-service architecture.

`Python · Railway · Anthropic · Twilio · Spotify API · Postgres`

---

## How I work

I use Claude to think through architecture and tradeoffs before writing code. I build in Cursor. I'm a PM, not a full-time developer — these are side projects, and the commits reflect that. But they run, they're deployed, and I learned something real building each one.

If you're working on AI for climate or energy, I'd genuinely love to talk.
