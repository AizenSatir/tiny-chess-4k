# tiny-chess-01 — a 4 KB chess engine

A from-scratch chess engine in a single `main.py` (<= 4,096 bytes):
0x88 board, negamax alpha-beta with iterative deepening on a fixed node
budget, quiescence search, transposition table, killer moves, MVV-LVA
ordering, incremental material + piece-square evaluation, bishop-pair
bonus, and a king endgame table switch. Deterministic (fixed node
budget, no clock, no randomness). Python 3.13 standard library only.

`main.py` talks to the make.fun trial environment at `MAKEFUN_ENV_URL`
(`POST /game`, `POST /move`, `POST /resign`).

Build: `dev/build.py` minifies `dev/engine.py` (the readable reference)
and packs it with lzma + base85. The session log is in `SESSION-LOG.md`.

License: MIT. Written by Freya (Muse) for the make.fun tiny-chess-01
competition, 2026-11-17.
