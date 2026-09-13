# 6-Hour DSA & C++ Mastery Tracker

A single-file, self-hosted dashboard for tracking a structured Data Structures & Algorithms study plan in modern C++ — built for a daily 3-block deep-work routine (Theory → Problem Solving → Review).

**Live demo:** [Planner](https://sohansourab.github.io/dsa/)

## Features

- **15-week / 7-phase roadmap** — C++ Core & STL → Linear Structures → Recursion & Binary Search → Trees & Heaps → Graphs → Dynamic Programming → Hard/Mock Sprints
- **Day detail view** — per-day goal, hour-by-hour 2.0h / 2.5h / 1.5h block breakdown, curated problem checklist, a key C++ idiom/snippet with one-click copy, and a personal notes field
- **Live dashboard stats** — completion %, hours logged, problems solved by difficulty, current phase — all computed from the actual curriculum data (no hardcoded/fake numbers)
- **Filters** — by phase, status (Pending / In Progress / Mastered), and free-text search across titles, goals, and problem names
- **Built-in focus timer** — 2h theory block, 50-minute grind sprints, 10-minute breaks
- **Progress auto-saves** to your browser (`localStorage`) — closing the tab or refreshing never loses your work
- **Export / Import** progress as JSON for backup or moving between browsers
- **Reset Progress** button to wipe the slate clean

## Running it locally

No build step, no dependencies to install. Just open the file:

```
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

Tailwind CSS and Google Fonts load from a CDN, so you need an internet connection the first time a browser caches them.

## Hosting on GitHub Pages

1. Create a new **public** GitHub repository.
2. Rename this file to `index.html` and upload it to the repo (Add file → Upload files → Commit changes).
3. Go to **Settings → Pages** → under "Build and deployment", set Source to **Deploy from a branch**, branch **main**, folder **/ (root)** → Save.
4. Wait ~1 minute — your tracker is live at `https://<your-username>.github.io/<repo-name>/`.
5. To update later: upload the changed `index.html` again and commit — GitHub Pages redeploys automatically.

## A note on progress storage

Progress is saved via your browser's `localStorage`, keyed to the page it's opened from. That means:

- Refreshing or closing the tab is safe — nothing is lost.
- Opening the same GitHub Pages URL from a different browser or device starts with a **separate, empty** progress state — `localStorage` does not sync across devices.
- Use the **Export** button periodically to back up progress as JSON, and **Import** to restore it (or move it to another browser/device manually).

## Current content coverage

The curriculum currently has **detailed content authored for 60 of the 105 roadmap days**, concentrated in Phases 1–4 (C++ Core, Linear Structures, Recursion/Binary Search, Trees/Heaps). Later phases (Graphs, DP, Hard/Mock Sprints) have sparser coverage with some day gaps — the header stats reflect this honestly (they're computed from the real data, not the original 105-day/630-hour claim). Filling in the remaining days is a good next step if you want the full roadmap fleshed out.

## Tech

Single HTML file — Tailwind CSS (CDN), vanilla JavaScript, no framework, no backend.
