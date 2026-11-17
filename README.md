# tiny-chess-01 entry

Original 0x88 chess engine in Python (MIT): alpha-beta + quiescence,
transposition table, killer ordering, piece-square eval.
`main.py` is the official `makefun compress` packing (LZMA,
makefun-compress/v1) of the minified dev source; it plays the env at
`MAKEFUN_ENV_URL` to a fixed 100,000-node budget per move, to depth 7. No clock, no
randomness, no model calls, no other files read. The transposition table is
bounded (cleared at each game start and when it passes 250,000 entries) so
memory stays well under the 512 MB limit. Piece-square tables follow the
house kit's MIT-licensed formula tables.
