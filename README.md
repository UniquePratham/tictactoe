# Tic Tac Toe

The classic game, built to be played in a browser tab. Two players, a win detector that handles all eight lines, and a reset that clears the board.

**Live:** https://prathamtictactoegame.web.app

## Features

- **Two-player** turn-based play on a 3×3 grid
- **Win detection** across all rows, columns and diagonals
- **Draw detection** when the board fills with no winner
- **Turn indicator** so it is always clear whose move it is
- **Reset** to start a new game without reloading
- Animated background and a custom favicon

## How it works

`Js/script.js` keeps the board as a flat array of nine cells and checks the eight winning lines after every move:

```
[0,1,2] [3,4,5] [6,7,8]   rows
[0,3,6] [1,4,7] [2,5,8]   columns
[0,4,8] [2,4,6]           diagonals
```

A move is rejected if the cell is already taken or the game has already been won, so the state cannot desync.

## Tech

Plain HTML, CSS and JavaScript with Font Awesome for the icons. No build step.

## Run locally

```bash
npx serve .
# or
python -m http.server 8080
```

Then open http://localhost:8080.

## Deploy

```bash
firebase deploy --only hosting --project prathamtictactoegame
```

## License

MIT — see [LICENSE](LICENSE).
