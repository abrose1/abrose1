# Hi, I'm Andrew

Product Manager at Paradox AI, now a Workday company following a successful acquisition, where I own the Conversational Scheduling product line that schedules roughly ~10% of all interviews in the US. Wharton undergrad, CS minor. [LinkedIn](https://www.linkedin.com/in/andrew-brose/)

I build side projects because AI is enabling an incredible era of innovation, and the best way to understand it is to build with it. Also it has become easier to build my own personalized solution for most problems than try to find an existing one.

I generally brainstorm with Claude then build with Cursor, but I try to shake it up every project to keep learning.

Below are my public projects. I have others that aren't, mostly because they contain my personal data.

---

## 🌍 [CarbonCoach](https://github.com/abrose1/CarbonCoach)

**Try it out [here](https://carboncoach.up.railway.app/)**

**Project summary on [LinkedIn post](https://lnkd.in/ew28SAhH)**

AI has a real carbon cost — and as someone who cares about emissions, that's always in the back of my mind. But AI can also be an incredible tool for fighting climate change, and I think we should be using it that way rather than shying away from it. CarbonCoach is my attempt to put that argument to work.

It's a conversational tool that calculates your personal carbon footprint, recommends personalized ways to reduce it, and searches 680 state and federal programs to surface financial incentives you may not know about (powered by the DSIRE database). Takes about 5 minutes and 15 messages to complete.

Each conversation emits ~7.8g of CO₂. A user who installs a heat pump or solar panels based on a recommendation reduces their footprint by ~4,000,000g/year. One in every ~500,000 users following through makes the app net-positive. The math makes me optimistic.

Built with Claude as the conversational interface. Full-stack: Flask, PostgreSQL, state-specific EPA emission factors.

`Python · Flask · Claude · PostgreSQL · HTML/CSS/JS`

---

## 📰 [AiNewsWatcher](https://github.com/abrose1/AiNewsWatcher)

Sends me one well-chosen SMS per day to keep me current on the AI industry — leaders, labs, tools, concepts, and the people shaping where this is all going. If something genuinely big breaks, that takes over the daily text instead.

As a PM in AI, staying fluent in the industry isn't optional. I built this because reading newsletters felt passive and not personalized enough — having something scan, filter, and surface what actually matters to me is more useful. Claude picks the topic, Brave Search finds the freshest angle on it, and the whole thing lands as a clean SMS. The hardest part by far was getting Twilio to approve my 10DLC to let me text myself.

`Python · Railway · Claude · Brave Search · Twilio · Postgres`

---

## ⚡ [ProjectBurnout](https://github.com/abrose1/ProjectBurnout) + [mcp-server-eia](https://github.com/abrose1/mcp-server-eia)

**Try it out [here](https://project-burnout.up.railway.app/)**

**Project summary on [LinkedIn post](https://lnkd.in/gaMgMxHY)**

Two connected projects born from the same weekend.

**Project Burnout** is a stranded asset dashboard tracking 100+ MW coal and gas plants across the U.S. Many are projected to operate at a loss for years after cheaper renewables should have replaced them — locked in by contracts, debt, and regulation. (And there are serious discussions about building *new* coal plants to power AI demand. That would be a very stupid move.) Burnout visualizes the gap between when each plant becomes unprofitable and when it actually shuts down, based on EIA filings and financial projections. Has a natural language query bar powered by Claude — I wanted to explore LLMs outside the chat interface, and I've found it genuinely useful.

**mcp-server-eia** started as practice building MCPs. The dashboard didn't end up needing one, so I built it anyway as a standalone tool. It's not a thin API wrapper — it's 10 domain-aware tools for querying plant inventory, generation mix, fuel prices, AEO projections, and state CO₂ emissions in a shape AI agents can actually use reliably. Free to use if you're building AI tools for energy or climate.

`Python · FastAPI · React · Claude · EIA API · MCP · Postgres`

---

## 📬 [ReleaseWatcherAgent](https://github.com/abrose1/release-watcher)

A scheduled agent that monitors new releases across books, music, TV, and film — and texts me when something worth paying attention to comes out. Runs on Railway Cron, polls Spotify, TMDB, Google Books, and Brave Search, then uses Claude to judge whether a release actually fits my taste before firing a Twilio SMS.

It reads from a private **taste-profile** repo that knows my favorite authors and artists, based on photos of my bookshelves and Spotify history. That repo isn't public (it has personal taste data in it), but the release-watcher README covers how the two-repo architecture works if you want to adapt it.

This one's purely for me — but it was a good excuse to build something with real multi-service architecture.

`Python · Railway · Claude · Twilio · Spotify API · Postgres`

---

## How I work

I use Claude to think through architecture and tradeoffs before writing code. I build in Cursor. I'm a PM, not a full-time developer — these are side projects, and the commits reflect that. But they run, they're deployed, and I learned something real building each one.

If you're working on AI or climate/sustainability, I'd genuinely love to talk. You can reach me on LinkedIn!
