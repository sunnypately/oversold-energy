# Oversold Energy Growth Monitor

Energy stocks with revenue up at least 20% year over year that trade at least 25% below their 52-week high, ranked by the gap between the live price and a blended fundamental fair value (earnings multiple, sales multiple, street target).

Live at: `https://sunnypately.github.io/oversold-energy/`

## Files

```
oversold-energy/
├── index.html               the page (tabs: All energy · Oil & gas · Power & clean energy · Method)
└── data/
    ├── fundamentals.json    names on the screen, with fundamentals and fair values
    └── not_on_screen.json   names checked that failed the screen, with the reason
```

## Deploy

1. Upload the `oversold-energy` folder to the root of the `sunnypately.github.io` repo (GitHub web UI: **Add file → Upload files**, drag the folder in).
2. Commit. GitHub Pages publishes it within a minute or two.

## Updating the data

Prices update live in the browser (Finnhub, every 5 minutes while open). Fundamentals and the screen are rebuilt each NYSE trading day on the Claude dashboard. To bring the GitHub copy up to date, replace the two files in `data/` with fresh exports and commit — `index.html` doesn't need to change.

The page needs to be served over http(s) (GitHub Pages or a local server such as `python3 -m http.server`); opening `index.html` directly from disk can't load the data files.

Research tooling, not investment advice.
