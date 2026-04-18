# Mafia Game PWA

> Multiplayer Mafia host controller — 17 roles, Monte Carlo balance simulator, React 19, Supabase.

<div align="left">

![React](https://img.shields.io/badge/React_19-1a1a1a?style=flat-square&logo=react&logoColor=cccccc)
![TypeScript](https://img.shields.io/badge/TypeScript-1a1a1a?style=flat-square&logo=typescript&logoColor=cccccc)
![Zustand](https://img.shields.io/badge/Zustand-1a1a1a?style=flat-square&logoColor=cccccc)
![Supabase](https://img.shields.io/badge/Supabase-1a1a1a?style=flat-square&logo=supabase&logoColor=cccccc)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-1a1a1a?style=flat-square&logo=tailwindcss&logoColor=cccccc)
![Vercel](https://img.shields.io/badge/Vercel-1a1a1a?style=flat-square&logo=vercel&logoColor=cccccc)

</div>

---

## Overview

A progressive web app built as a host controller for live Mafia games. The problem: managing complex role assignments, game phases, and artifact interactions in real time across 10–15 players is error-prone with paper. This app handles the full game lifecycle — role distribution, night phase resolution, artifact card management, and session cloud sync.

Shipped on Vercel as a PWA — works offline, installable on any device.

---

## Architecture

```
MafiaApp (React 19 + TypeScript)
├── GameEngine
│   ├── RoleSystem         — 17 roles, deterministic rule enforcement
│   ├── PhaseController    — day/night cycle, voting, elimination logic
│   ├── ArtifactDeck       — 16 cards with effect resolution
│   └── MonteCarloSim      — 1,000-game balance simulator
├── State Layer
│   ├── Zustand stores     — game state, player state, settings
│   └── Supabase sync      — real-time session persistence
├── UI Layer
│   ├── HostPanel          — game master control interface
│   ├── PlayerView         — role reveal, action tracking
│   └── HistoryLog         — full game transcript
└── PWA config             — offline support, installable
```

---

## Key Features

- **17 roles** — full role set including special, faction, and solo roles
- **16 artifact cards** — unique effects resolved by game engine automatically
- **Monte Carlo simulator** — 1,000-game statistical balance analysis per role configuration
- **Real-time sync** — Supabase Realtime for live session state across devices
- **PWA** — installable, works offline, no app store required
- **Deterministic engine** — all rules enforced by code, no host judgment calls needed
- **Game transcript** — full action history exportable per session

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | React 19 |
| Language | TypeScript |
| State | Zustand |
| Backend | Supabase (Postgres + Realtime) |
| Styling | Tailwind CSS |
| Deploy | Vercel |
| PWA | Vite PWA plugin |

---

## Metrics

- **10,000 LOC** — total codebase
- **17** roles implemented
- **16** artifact cards
- **1,000-game** Monte Carlo simulator
- Deployed live on Vercel

---

More at [0xgrek.com](https://0xgrek.com/projects/mafia-game-pwa)

---

MIT License
