# Word Search America

A mobile-first American word-search game: Adventure chapters, America Super Mix, Daily Puzzle, Free Play, combos and America Fever, and a Culture Profile with badges and bonus trivia.

## Files

| File | Size | Used for |
|---|---|---|
| `index.html` | single file | The whole game: HTML, CSS, JavaScript and the embedded Overpass font |
| `logo.png` | 1400 × 1240, transparent | Home screen and launch screen logo (designed for the navy background) |
| `app-icon-1024.png` | 1024 × 1024, opaque, square corners | App Store icon master (Xcode / App Store Connect) |
| `apple-touch-icon.png` | 180 × 180, opaque | iPhone "Add to Home Screen" icon |
| `favicon.png` | 32 × 32 | Browser tab icon |
| `favicon-16.png` | 16 × 16 | Small browser tab icon |

Keep all six files in the same folder. `index.html` loads the images with relative paths.

## Publish on GitHub Pages

1. Create a repository (for example `word-search-america`) and upload all six files to the root.
2. In the repository, open **Settings → Pages**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
3. The game appears at `https://<your-username>.github.io/word-search-america/` after a minute or two.

## Player data

Progress and settings are saved in the browser's localStorage under the key `wordSearchAmerica.save`. Older saves are upgraded automatically. All repositories on the same `github.io` address share one storage area, but the key is unique to this game.

## Known limits of the web version

- No offline play yet (that needs a service worker file).
- Progress is stored per device and per browser; there is no cloud sync.
- Safari can clear website data after about 7 days without a visit. Playing from the Home Screen icon avoids this.
- The iPhone silent switch mutes the sound effects.
- An App Store release needs a native wrapper (for example Capacitor) and an Xcode build. `app-icon-1024.png` is ready for that step.
