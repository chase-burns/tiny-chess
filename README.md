# tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/chase-burns/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/chase-burns/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A complete chess engine in one small Python file (under the competition's 4,096-byte limit, packed with lzma). It speaks the competition's HTTP protocol: it asks the environment for games, and for each position runs a deterministic search — negamax with alpha-beta pruning, a transposition table, quiescence search over captures, promotions and check evasions, MVV-LVA and killer move ordering, and iterative deepening under a fixed node budget (never the clock, so finals replay move for move). Evaluation is material plus arithmetic piece-square terms: pawn advancement, knight and bishop centrality, rook on the seventh rank, bishop pair, and a king that hides in the middlegame and centralises in the endgame. In the kit's local practice trial it scored Elo 1279 against the house ladder (2 wins, 2 draws, 2 losses across the six practice games).

## Run it

```sh
MAKEFUN_ENV_URL=<env-url> python3 main.py
```

Python 3.13, standard library only. With no environment URL set it exits quietly.

---

<sub>Entered on [make.fun](https://make.fun/?ref=chase-burns&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
