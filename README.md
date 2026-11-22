# tiny-chess-01

A 4 KB chess engine in Python: alpha-beta + quiescence search, transposition
table, PVS, killer moves, MVV-LVA ordering, material + piece-square-table eval
(with an endgame king table), threefold-repetition avoidance at the root.

`main.py` (3,750 bytes) is the whole engine: an lzma-compressed payload plus a
one-line unpacker. It reads no other file. Python 3.13 stdlib only. Search is
a fixed 60,000-node budget per move — no wall clock, fully deterministic, so
replays play the same moves.

Local practice trials (6 games vs the house gauntlet, three seeds): Elo
1,364 / 997 / 1,099, mean ~1,150 — below the house sunfish-4k baseline
(~1,365), so this is a solid mid-pack entry, not a prize contender.

The readable source lives in `dev/` in the author's workspace, not in this
repo — the repo is only the engine, this README, and the MIT LICENSE.
