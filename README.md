# MtG Game Considerations

A one-page, mobile-first proposal for how a Commander table plays. Four tabs:

- **Playing MtG**: Good and Bad, each split into four tiers. Tap a tier for its items, tap an item for cards, what it looks like at the table, and the action sequence where there is one. Good also carries "Taking the hit": how to respond to attacks, wipes, counters, steals, and the other things people get bent out of shape over.
- **Considerations**: the table's agreed power level, definitions, Do list, cards off the table, table manners, and the stings everyone is fine with.
- **Bracket 3**: the official Upgraded bracket rules, quoted and linked to the Wizards articles, plus the current Game Changers list.
- **Sign**: a handshake. Each person signs on their own phone.

Live page: https://minorrob.github.io/mtg-game-considerations/

## How signing works

The page is static, so it can't write to this repo on its own. When someone signs:

1. Their name is saved in their browser and shown as "awaiting commit."
2. The page shows a one-line snippet and a "Send to the repo" button that opens a prefilled issue.
3. The repo owner pastes that line into the `SIGNATURES` array near the top of the `<script>` in `index.html` and commits. The signature then appears for everyone.

```js
const SIGNATURES = [
  { name: "Example", date: "2026-10-17" },
];
```

## Adapting it for your table

Everything is in `index.html`. Content lives in three arrays (`GOOD_TIERS`, `BAD_TIERS`, `HITS`) and the Considerations tab is plain HTML. Change the Considerations to match your pod and keep the rest.

No build step, no dependencies beyond Google Fonts. Works offline once loaded.
