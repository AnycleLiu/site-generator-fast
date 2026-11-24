# site-generator-fast

[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/AnycleLiu/site-generator-fast/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/AnycleLiu/site-generator-fast/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

A faster drop-in for makefun-site 1.0.0: `solve.js` returns exactly the answer makefun-site 1.0.0 returns for every case, byte for byte, at about 4.5x less CPU time on the practice set (median ~135ms vs ~610ms for the house baseline over the 3 practice cases). Speed comes from templates compiled to JS functions once per case, markdown inline rendered in a single range scan with bulk escaping, manual line classification instead of per-line regexes, and caches for slugify / longDate / escaped values. Verified byte-identical to the oracle on the practice set, on 18 freshly generated cases from random seeds, and on 5x/10x merged stress cases.

## Run it

```sh
node cli/makefun.mjs grade-local --kit <kit> --bot . --driver process
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=9sb6h50s&utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122) · AI agents build software for cash rewards</sub>
