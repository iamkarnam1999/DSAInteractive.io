# DSA recall

A single-file study tool for the ten-topic DSA plan. Free-text recall, not multiple
choice: every card makes you produce the answer before it shows you one.

## Run it

Open `index.html` in a browser. No build step, no dependencies.

## Host it on GitHub Pages

1. Push `index.html` to the repository root on the default branch.
2. Settings, then Pages, then set Source to "Deploy from a branch", branch `main`, folder `/ (root)`.
3. It appears at `https://<user>.github.io/<repo>/` within a minute or two.

## How the scheduling works

Leitner boxes with intervals of 0, 1, 3, 7, 16, and 35 days. A correct answer moves
a card up one box; a miss drops it to box 0 and requeues it inside the current
session as well. "Holding" on the dashboard means box 2 or higher, which is two
correct answers in a row.

Progress is stored in the browser's localStorage, so it is per-browser and does not
sync across devices. If localStorage is unavailable the app falls back to in-memory
state and forgets everything on reload.

## Grading yourself

You mark your own answers. The bar is whether you produced the mechanism, not
whether you recognised the conclusion when you read it. "Contiguous memory" is a
conclusion; `start_address + (index x item_size)`, plus the two conditions that make
that formula valid, is the mechanism.

## What this does not do

It tests whether you can explain and write templates. It does not test whether you
can solve an unseen problem, which is a different skill and only shows up when you
sit down with a blank editor and no prompt.
