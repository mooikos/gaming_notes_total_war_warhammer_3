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

## Repository Structure (`docs/`)
- `docs/index.md` — Home page (`nav_exclude: true`)
- `docs/campaigns/` — Campaign tracking, Immortal Empires lord counts, lord randomization, completed campaigns
- `docs/general/` — General terminology/descriptions, generic traits, unit types, unit roles, army compositions
- `docs/items/` — Equipment & banners (`armour`, `weapon`, `talisman`, `enchanted-item`, `arcane-item/`, `banner`). Subfolders like `docs/items/arcane-item/` split items into `generic.md` (all magic races) and race-specific pages (e.g., `dark-elves.md`, which includes both race-exclusive and multi-race/lore-specific items available to that race), ordered incrementally by rarity in tables with inline ability descriptions.
- `docs/races/` — Race-specific guides, factions/legendary lords, generic lords & heroes, buildings, traits, unit caps, unit roles, and counters

## Formatting & Naming Conventions
- **File names & Permalinks**: Use `kebab-case` (e.g., `armies-compositions.md`, `permalink: general/armies-compositions`). Avoid leading underscores (`_`) in content file names so Jekyll does not ignore them.
- **In-note identifiers**: Use `snake_case` for unit names, stats, abilities, and traits inside note bodies (e.g., `damage_armour_piercing`, `black_ark_corsairs`), matching `docs/general/descriptions.md`.
- **Markdown quality**: Ensure proper heading hierarchy (`#` -> `##` -> `###`), valid list indentation, escaped special characters where needed, and valid relative/permalink URLs.
