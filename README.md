# NUMBAT hackathon 2026: `charades()` icebreaker

Slides for the opening icebreaker of the NUMBAT hackathon 2026. In groups, people act out R
functions without talking while their team guesses. About 28 people play in 6 groups.

### Structure

The icebreaker takes 30 minutes:

* Form groups: 6 groups of 4–5 people (3 min)
* How it works: `icebreaker::charades` printed as an R function, revealed step by step (3 min)
* Rules: no talking, hints allowed, skip a card if someone talks or cheats, 3 minutes per round, and the most words wins (2 min)
* Demonstration: three example words against a 1 minute timer (2 min)
* Rounds 1–4: 3 minute countdowns, each followed by a score card, with time between rounds to swap actors and cards (17 min)
* Final scores: the score card after round 4, with the winner highlighted (3 min)

### Rendering the slides

The slides are written with [Quarto](https://quarto.org), and the extension
they use is included in this repository. Preview them with:

```bash
quarto preview index.qmd
```

This renders to one self-contained `index.html` that works offline. For PDF,
open the deck with `?print-pdf` in Chrome and print with background graphics on.

Each round is a 3 minute countdown slide (`{.break minutes=3}`) that starts
when the slide is shown. The demonstration slide (`{.practice}`) reveals each
word as a fragment. Its 1 minute timer starts when the first word is revealed,
and you can click it to restart.

The score card slides (`{.scores data-round=n}`) all share one table. Type the
group names and each round's scores into any of them; the totals add up
automatically and the scores are saved in the browser, so they survive a reload.
Enter moves down a column and Escape leaves a field so the arrow keys move between
slides again. Shift-click the Total heading to clear everything before the event.

### Files

* `index.qmd`: the slides
* `charades.css`: the deck's own styles
* `practice.html`: the demonstration timer
* `scores.html`: the score cards
* `_extensions/numbat/`: slide styles adapted from the WOMBAT 2026 slides to match [numbat.space](https://numbat.space): Source Sans, light backgrounds with midnight blue, blue and blood orange highlights, and the numbat from the website banner
* `2025-questions.pdf`: last year's cards
* `2026-questions.html`: draft cards for this year, still to be discussed
