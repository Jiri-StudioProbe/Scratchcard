# Scratchcard

Scratch off the paper to reveal a Wikipedia summary. Single file (`index.html`), no build, no dependencies. Deployed to GitHub Pages from `main`.

## Interests and history

- **Onboarding:** three refining steps (broad theme, narrower, narrowest) pick what cards are drawn from. The taxonomy is the `TREE` constant in `index.html`; only the narrowest level maps to a Wikipedia category.
- **Cards:** for each card the app picks a leaf under your picks (weighted by what you read vs skipped), asks Wikipedia for random articles in that category, and shows one you haven't seen. About 15% of cards are plain random.
- **Suggestions:** every 3 cards a "More like this?" screen offers narrower or sibling topics to add.
- **History:** every card is recorded as `shown`, `read` (Read more tapped) or `ignored` (New card tapped without Read more), with the max scratch percentage. See it under the **History** link.
- Everything is stored in `localStorage` on the device (key `scratchcard.v1`). Tune the behaviour with the constants at the top of the script (`SUGGEST_EVERY`, `EXPLORE_RATE`, ...).

Editing `TREE`: ids are slugs of the labels, so renaming a label drops anyone's stored picks for it.
