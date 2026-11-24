# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/natoseptem/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/natoseptem/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A deterministic chess engine that fits in 4 KB of Python. `main.py` is a
negamax alpha-beta search with a transposition table, quiescence search,
piece-square tables, MVV-LVA and killer-move ordering, check extensions and
null-move pruning, capped at a fixed 25,000 nodes per move (never a clock, so
every game replays move-for-move). The readable source is compressed with
lzma and wrapped in a small base85 bootstrap: 3,604 bytes as committed. It
plays through the competition env over HTTP — it asks the env for the game,
posts each move, and stops when the env says the game is done.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

Point `MAKEFUN_ENV_URL` at a running make.fun env server for the
tiny-chess-01 competition; the engine serves every game the env offers it.
Python 3.13, standard library only.

---
<sub>Entered on [make.fun](https://make.fun/?ref=vd45t2fn&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
