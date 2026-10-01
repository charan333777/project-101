# Side Quest
A small, free website for everyday adventures and life upkeep, with a weekly bingo board.

## Use it
Download the repository and open index.html in a modern browser. No installation, build step, account, API key, or network request is required.

## Publish with GitHub Pages
The workflow in .github/workflows/pages.yml publishes index.html using GitHub's official Pages actions. It runs when the website or workflow changes on main, and can also be started manually.

For one-time setup, open [Settings → Pages](https://github.com/charan333777/project-101/settings/pages) and select GitHub Actions as the Source under Build and deployment. The workflow also attempts automatic Pages enablement if its GitHub token permits it.

Open [Actions → Publish Side Quest](https://github.com/charan333777/project-101/actions/workflows/pages.yml) to start or retry publication. A successful deployment displays the live URL: https://charan333777.github.io/project-101/. The URL is only live after Pages has been enabled and the deployment succeeds.

If a run fails before any steps execute, open its summary and inspect GitHub's annotations. Resolve any account, Actions, or environment restriction GitHub reports before rerunning. If Configure GitHub Pages fails with a permission error, enable Pages in Settings as described above. No personal access token is required for normal deployment.

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
