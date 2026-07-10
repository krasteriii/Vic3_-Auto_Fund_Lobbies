# Auto Fund Lobbies (Victoria 3 mod)

If the player has enough Influence, it will automatically fund lobbies abroad — if enabled.

A permanent **journal entry** (*Automated Lobby Funding*, under Foreign Affairs) acts as the settings panel:

- **Enable / Disable Automation** — off by default; one click to turn on.
- **Check Now** — runs one automation check immediately instead of waiting for the weekly tick; hover it to preview exactly what it will do.
- **Protected Influence reserve** — Influence the automation will never spend. Adjustable between **50 and 500** in steps of 50 (default 100).

## What the automation does

Once per week, while enabled:

1. **Cleans up** — forgets any automated pact that already broke on its own (war, bad relations, rank loss...).
2. **Below the reserve?** Cancels the least valuable automated *Fund Lobbies* pact (one per week) until available Influence is back above the reserve. Pacts you created manually are **never** touched.
3. **Comfortably above the reserve?** Creates one new *Fund Lobbies* pact per week with the best candidate country, preferring countries that already host a lobby friendly to you, your subjects, and members of your power bloc, then higher-ranked countries.

Costs are estimated per target rank (a great power pact costs 200 base Influence, a major power 150, others 100, multiplied by your infamy level plus a 15% margin), so a new pact is only created when it should not drop you below your reserve — e.g. with no infamy, funding a minor power needs about 115 spare Influence above the reserve, a great power about 230. Because *Fund Lobbies* pacts also transfer money, new pacts are only created while your weekly balance is positive, you are not in default, and your debt is below 25% of your gold reserve limit (the same threshold at which the vanilla AI cancels these pacts).

## Requirements

- Victoria 3 **1.13.x**
- **Sphere of Influence** DLC (the `lobbies` feature — the journal entry only appears with it)
- The journal entry activates once you research **Central Banking** (the tech that unlocks *Fund Lobbies*)

## Localization

Fully localized in all 11 supported languages: English, Brazilian Portuguese, French, German, Japanese, Korean, Polish, Russian, Simplified Chinese, Spanish, Turkish — reusing vanilla terminology via game concepts.

## Installation

Copy the mod folder (containing `.metadata/`, `common/`, `localization/`) into:

```
Documents/Paradox Interactive/Victoria 3/mod/Auto_Fund_Lobbies/
```

then enable **Auto Fund Lobbies** in a playset in the launcher. Works in multiplayer (each human player gets their own journal entry and settings) and can be added to an existing save.
