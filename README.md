# CCS design

Shared design tokens for the CCS sites, so they look the same and can later be merged into one site.

**Stylesheet:** `ccs-tokens.css`, served at https://zefanonuevo.github.io/ccs-design/ccs-tokens.css

Used by:
- [ccs-task-tracker](https://github.com/zefanonuevo/ccs-task-tracker)
- [ccs-scgss](https://github.com/zefanonuevo/ccs-scgss)

## What it contains
- Color, shadow, easing and type tokens, in light and dark.
- The System / Light / Dark theme switch styles (`.theme`).

Theme selection: no `data-theme` attribute follows the device setting. `data-theme="light"` or `"dark"` overrides it. Each page applies the saved choice from `localStorage` (`ccs-theme`) with a small inline script before first paint.

## Using it
```html
<link rel="stylesheet" href="https://zefanonuevo.github.io/ccs-design/ccs-tokens.css?v=1">
```
Put it before the page's own `<style>`. Raise the `?v=` number after changing the file, because GitHub Pages caches for about 10 minutes.

App-specific tokens (chart colors, status dots) stay in each app.

## Note
Pages that load this file need a network connection. Opened offline, the tokens are missing and the page loses its colors.
