# Nudge Advent 2026

A digital advent calendar from Nudge Education: twenty-four doors, one for each day of December up to Christmas Eve. Made for fun.

Served by GitHub Pages from this repository. `index.html` does all the work (no build step, no dependencies beyond two Google Fonts).

## Two editions, one page

- **Everyone** (families, young people, commissioners): the plain address. Each door holds a thought on a life worth living and a cracker joke or quiz question.
- **Staff**: the same address ending in `#staff`. It asks for the staff word from the December Monthly Nudge, then shows the staff lines, that day's socials, drop-ins and training, and a banner.

The staff content is in `staff.bin`, encrypted with the staff word (AES-GCM, key derived with PBKDF2). This repository is public, so the readable source for it is kept outside the repository and must not be committed here. The same goes for anything else added: no links to sign-up forms or internal documents, no venues, no personal names, and nothing about young people.

## Checking doors early

Each door opens from its own date in December 2026, in the visitor's local time. To check every door before then, end the address with `#preview` (or `#staff-preview` for the staff edition).

## Editing

The public words are in two lists near the bottom of `index.html`: `LINES_PUBLIC` and `CRACKERS`, each in date order. The staff edition is rebuilt from its source folder with `encrypt.mjs`, which writes a new `staff.bin`.

Adapted from the Twenty-Four Doors calendar at TheNovacene/advent-site.
