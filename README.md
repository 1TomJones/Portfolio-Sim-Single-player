# welcome-fair

Single-player local trading sim focused on a 6-month macro scenario.

## High level architecture

| Layer | Purpose |
| --- | --- |
| **`server.mjs`** | Express + Socket.IO host that runs one local player session and streams market/portfolio updates. |
| **`public/`** | Player-facing UI with briefing, trading workspace, and end-of-run results. |
| **`src/engine/`** | Market core handling order execution, PnL, and tick-driven simulation logic. |

## Getting started

```bash
npm install
npm start
```

Open `http://localhost:10000`.

## Single-player flow

* Player is prompted to enter fullscreen on launch.
* Player enters their name and the simulation starts instantly.
* Scenario is fixed to **`macro-six-month`**.
* A top-bar countdown timer shows time remaining (`MM:SS`) based on ticks left at 10 ticks/sec.
* End-of-sim metrics and result charts are shown automatically.
