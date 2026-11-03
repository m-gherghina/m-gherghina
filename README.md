# Mircea Gherghina — personal website

Built with [Quarto](https://quarto.org). The finished site is in `docs/`.

## Files you edit
- `index.qmd` — bio, plus the Research tab and the Teaching tab
- `profile.jpg` — your photo (replace the placeholder; a portrait or square photo works)
- `cv.pdf` — your CV (replace with the newest version, same name)
- `_quarto.yml` — site settings and theme
- `styles.css` — style tweaks (tabs, colors, spacing)
- `tabs.html` — the small script that makes the Research / Teaching tabs work (no need to edit)

## How the tabs work
In `index.qmd`, each tab is a block that starts with
`:::: {#research .tab-section data-tab="Research"}` and ends with `::::`.
The `data-tab` text is the tab's label. To add a third tab (say, "Talks"), copy that pattern:

    :::: {#talks .tab-section data-tab="Talks"}
    ## Invited talks
    ...
    ::::

You can link straight to a tab: `yoursite/#teaching`.

## Collapsible abstract / summary
Put this inside a paper's block, before its closing `:::`:

    ::: {.callout-note collapse="true" appearance="simple" icon="false"}
    ## Abstract
    Paste the abstract here.
    :::

## Update the site
1. Edit the files above.
2. In this folder, run: `quarto render`
3. Commit and push. GitHub Pages serves the `docs/` folder.
