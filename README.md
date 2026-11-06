# Padel_score — Xiaomi Smart Band 10

Padel score tracker built as a Xiaomi Vela JS quick app (212×520 screen).

## Features
- Points / games / sets, always golden point at 40-40, 7-point tie-break at 6-6
- Best of 3 sets: when a team takes 2 sets the match is saved to history, a WON/LOST banner shows for 4 s and a new match starts
- Serve indicator (`SRV R` / `SRV L`), tap the SETS/GAMES area at 0-0 to swap the first server
- US in blue, THEM in red; SCREEN ON/OFF button on top; UNDO and HISTORY at the bottom
- Undo (last 30 points, in memory only) can also undo the point that ended a match
- HISTORY shows the last 10 matches with date, start time and duration; long-press HOLD: NEW MATCH to end the current match early (saved if a game was played, undoable), long-press HOLD CLEAR to wipe the history

## Build
```
npm install
npm run build      # debug package -> dist/*.debug.*.rpk
npm run release    # signed package, uses sign/ (never commit sign/)
```

## Install
Copy the `.rpk` to an Android phone and sideload it with Notify for Xiaomi.

## Notes
- Keep `src/common/logo.png` small (80×80 round PNG with transparent corners, a few KB). A 1254×1254 icon made the band reboot-loop.

## License
[ISC](LICENSE)
