# Contemporary

An Obsidian theme, currently a blank scaffold — `theme.css` has every CSS
variable commented out, so as-is it changes nothing. Fill it in incrementally.

## Developing

This folder already lives at `.obsidian/themes/Contemporary` inside the vault
you're editing it from, so Obsidian picks it up automatically:

1. Settings → Appearance → Themes → select **Contemporary**.
2. Edit `theme.css`, save, and reload Obsidian (`Cmd/Ctrl+R` via the command
   palette's "Reload app without saving") to see changes.
3. Toggle Settings → Appearance → Base color scheme between light/dark to
   check both `.theme-light` and `.theme-dark` blocks.

Reference for available variables: https://docs.obsidian.md/Reference/CSS+variables

## Publishing to GitHub

```bash
cd "/Users/johnmorabito/Documents/Dev Vault/.obsidian/themes/Contemporary"
gh repo create jsmorabito/obsidian-contemporary --public --source=. --remote=origin
git push -u origin main
```

## Submitting to the Obsidian community theme browser

Once the theme is in a good state:

1. Make sure `manifest.json` and `theme.css` are at the **root** of the repo
   (they are, here) and `version` in `manifest.json` is bumped.
2. Add a screenshot (`screenshot.png`, ~1024px wide) showing the theme in use.
3. Fork [obsidianmd/obsidian-releases](https://github.com/obsidianmd/obsidian-releases)
   and add an entry to `community-css-themes.json`:

   ```json
   {
     "name": "Contemporary",
     "author": "jsmorabito",
     "repo": "jsmorabito/obsidian-contemporary",
     "screenshot": "screenshot.png",
     "modes": ["dark", "light"]
   }
   ```

4. Open a PR against `obsidian-releases`. The bundled bot checks your repo
   structure automatically (manifest fields, license, root-level files).
5. Add a `LICENSE` file (MIT included here) — required for submission.

Full guidelines: https://docs.obsidian.md/Themes/App+themes/Submit+your+theme
