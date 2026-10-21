# LTM Group website figures

`stats.json` holds the figures shown on the home page of https://www.ltm-group.co.uk.

When a job completes: `projects_completed` up by one, `projects_ongoing` down by one, commit. The website reads this file directly, so the new figures appear within about five minutes. No rebuild is needed.

- `founded`: the year LTM was founded; "Years in business" is worked out from it.
- `apprentices_trained`, `projects_ongoing`, `projects_completed`: whole numbers. Set one to `null` to hide its tile.
- `projects_completed_show_plus`: `true` shows "1,000+", `false` shows the exact number.

Keep the file valid JSON (quotes around names, commas between lines). If it can't be read, the site falls back to the last built figures.
