# Side Quest
A small, free website for everyday adventures and life upkeep, with a weekly bingo board.

## Use it
Download the repository and open index.html in a modern browser. No installation, build step, account, API key, or network request is required.

For a public website, open this repository's Settings → Pages. Under Build and deployment choose Deploy from a branch, then main and / (root), and save. GitHub will display the published URL after deployment. Committing files alone does not enable Pages.

## Features
- 24 curated quests: adventure and life upkeep.
- Filter by available time (5, 15, or 30 minutes), energy, and mood.
- Three suggestions with swapping, completion, and undo.
- A deterministic weekly 3×3 bingo board, refreshed on local Monday.
- Bingo quest details, completion, row/column/diagonal detection, and a confirmed board reset.
- Progress in browser localStorage. No analytics or external assets.

Quest history and bingo checkmarks are separate: undoing a quest card does not erase a bingo checkmark, and undoing a bingo checkmark retains quest history. Resetting the board also retains quest history.
Progress is local to each browser and origin; clearing browser data removes it. Browser restrictions can prevent saving; the app reports this and keeps session progress. Opening locally and visiting the hosted site use separate storage.

## Implementation
One self-contained index.html with semantic HTML, responsive CSS, native dialogs, and vanilla JavaScript. Edit the quests array to add or adjust content.

## Validation
JavaScript syntax checked. All 27 filter combinations have at least three matching quests. Interaction checks using a simulated DOM covered completion, undo, swaps, filter eligibility, bingo detection, persistence writes, and reset preserving history. No real-browser visual or accessibility audit was available in the build session.

## Next ideas
Custom quests, optional board tile replacement, progress export, and broader browser testing.
