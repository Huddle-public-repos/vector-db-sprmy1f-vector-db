# Huddle room

This repository backs a [Huddle](https://github.com/kishorebhatia/huddle-ai-collab) room. Huddle writes the room's
brief, decisions, research and prototypes here automatically as the room works (and when someone presses **Publish to GitHub**).
Public rooms live in the Huddle-public-repos organization; anything in them is public.

| Path | What it holds |
|---|---|
| `BRIEF.md` | The room's living brief: goal, decisions, open questions, next steps |
| `decisions/` | Decisions the team locked |
| `research/` | Research the agents ran, with sources |
| `prototypes/<name>/` | Code the agents built, as deployed |
| `deploy.md` | Where each prototype is live, with its smoke test and eval scores |
| `transcript/` | Only if the room chose to include it |

Prototypes are also served by GitHub Pages from this repository (public repositories only).
