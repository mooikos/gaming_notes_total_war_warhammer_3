# AGENTS.md — Total War: Warhammer 3 Gaming Notes

## Project Overview
We organize, maintain, and expand structured Markdown (`.md`) gaming notes for **Total War: Warhammer 3** in this repository (`gaming_notes_total_war_warhammer_3`).
The site is built with Jekyll using the [Just the Docs](https://just-the-docs.com) theme from the `docs/` directory and hosted on GitHub Pages (`https://mooikos.github.io/gaming_notes_total_war_warhammer_3`).

## Core Principle: Always Keep Everything Up-to-Date
- **Always keep all files and references up-to-date.** Whenever you create, edit, rename, or remove a `.md` file:
  1. Update `docs/index.md` and the relevant section `index.md` (`docs/campaigns/index.md`, `docs/general/index.md`, `docs/items/index.md`, `docs/items/<item-type>/index.md`, `docs/races/index.md`, `docs/races/<race>/index.md`).
  2. Verify Jekyll frontmatter (`permalink`, `parent`, `grand_parent`, `nav_order`, `has_children`) matches the folder hierarchy and link targets.
  3. Check and update cross-links across all `.md` files and `README.md` so no broken links or stale references exist.
  4. Keep this `AGENTS.md` file up-to-date whenever project structure, conventions, or workflows evolve.
- **Authoritative Game Data Source:** Cross-check item, trait, unit, and ability data against [TWDB (`twdb.io/warhammer3/database/`)](https://twdb.io/warhammer3/database/items/) and the [Total War: Warhammer Wiki](https://totalwarwarhammer.fandom.com/wiki/Total_War:_Warhammer_items).
- **Tabletop Caps Mod Convention:** All army compositions (`docs/general/armies-compositions.md` and race Lord pages) follow Tabletop Caps rules: 20 units total (`1` Lord + `3-4` Heroes + `15-16` units), unlimited **Common** (`0` pts), max **10 Special points** (`Special 1..3`), and max **5 Rare points** (`Rare 1..3`).

## Repository Structure (`docs/`)
- `docs/index.md` — Home page (`nav_exclude: true`)
- `docs/campaigns/` — Campaign tracking, Immortal Empires lord counts, lord randomization, completed campaigns
- `docs/general/` — General terminology/descriptions, generic traits, unit types, unit roles, and generic army composition archetypes (`armies-compositions.md`)
- `docs/items/` — Equipment, banners & followers (`armour/`, `weapon/`, `talisman/`, `enchanted-item/`, `arcane-item/`, `banner/`, `follower/`). Each category subfolder splits items into `generic.md` and race-specific pages (e.g., `dark-elves.md`), ordered incrementally by rarity in tables with inline ability/unlock descriptions.
- `docs/races/` — Race-specific guides (e.g., `docs/races/dark-elves/`), organized into:
  - Factions / Legendary Lords (e.g., `lokhir-fellheart.md`)
  - `lords/` — Generic Lords and their Tabletop-Caps army compositions (`dreadlord.md`, `dreadlord-crossbow.md`, `high-beastmaster.md`, `supreme-sorceress.md`)
  - `heroes/` — Generic Heroes (`death-hag.md`, `khainite-assassin.md`, `master.md`, `sorceress.md`)
  - Race-specific mechanics & tables (`buildings.md`, `names-of-power.md`, `traits.md`, `unit-caps.md`, `unit-roles.md`)
  - `counters/` — Matchup counter notes

## Formatting & Naming Conventions
- **File names & Permalinks**: Use `kebab-case` (e.g., `armies-compositions.md`, `permalink: general/armies-compositions`). Avoid leading underscores (`_`) in content file names so Jekyll does not ignore them.
- **In-note identifiers**: Use `snake_case` for unit names, stats, abilities, and traits inside note bodies (e.g., `damage_armour_piercing`, `black_ark_corsairs`), matching `docs/general/descriptions.md`.
- **Markdown quality**: Ensure proper heading hierarchy (`#` -> `##` -> `###`), valid list indentation, escaped special characters where needed, and valid relative/permalink URLs.
