# Contemporary

An Obsidian theme, built up one change at a
time. See the header of `theme.css` for what's in so far.

## Companion plugin

The left sidebar's Files row gets a hover "..." menu (new note, new folder, sort order,
expand/collapse...) from the **Contemporary Theme Settings** plugin. The theme works
without it; the explorer just keeps its normal button row.

## Developing

This folder lives at `.obsidian/themes/Contemporary` inside the vault you edit it from,
so Obsidian picks it up automatically:

1. Settings → Appearance → Themes → select **Contemporary**.
2. Uncheck Settings → Appearance → **Show ribbon** for the full effect.
3. Edit `theme.css`, save, and reload Obsidian ("Reload app without saving" in the
   command palette) to see changes.
4. Check both light and dark under Settings → Appearance → Base color scheme.

Reference for available variables: https://docs.obsidian.md/Reference/CSS+variables

## Publishing to GitHub

```bash
cd "/Users/johnmorabito/Documents/Dev Vault/.obsidian/themes/Contemporary"
gh repo create jsmorabito/obsidian-contemporary --public --source=. --remote=origin
git push -u origin main
```

## Submitting to the Obsidian community theme browser

Once the theme is in a good state:

1. Make sure `manifest.json` and `theme.css` are at the **root** of the repo (they are,
   here) and `version` in `manifest.json` is bumped.
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

4. Open a PR against `obsidian-releases`. The bundled bot checks your repo structure
   automatically (manifest fields, license, root-level files).
5. `LICENSE` (MIT) is included, which is required for submission.

Full guidelines: https://docs.obsidian.md/Themes/App+themes/Submit+your+theme
