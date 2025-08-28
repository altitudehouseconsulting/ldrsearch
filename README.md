# Sanford LDR Search — Deployment Package (HTML-only)

This package includes the **HTML app** and **index redirect**. Your dataset JSON already lives in your repo.

## Files in this package
- `index.html` — redirect to the app (preserves query/hash)
- `ldr-search-table-branded-deeplink-tools-print.html` — app with deep links, copy/export tools, print view

## Where to place them
Upload both files **into the same folder** as your dataset JSON in your repo (you already have):
- `sanford_ldr_schedules_master_ALL_concatenated_with_subsections.json`

If your repo is `altitudehouseconsulting/ldrsearch`, that means the **repo root**.

## GitHub Pages settings
- **Settings → Pages**
  - **Source**: your branch (e.g., `main`)
  - **Folder**: `/ (root)` (since your files are in the repo root)

## How to open
- Root: `https://<your-user>.github.io/<your-repo>/`
- Direct: `https://<your-user>.github.io/<your-repo>/ldr-search-table-branded-deeplink-tools-print.html`

## Data path robustness
The app tries multiple dataset paths automatically, including the filename you have now. If you ever move the JSON, you can force a path with:
```
?data=relative/path/to/your.json
```
Example:
```
https://<your-user>.github.io/<your-repo>/?data=data/sanford_ldr_schedules_master_ALL_concatenated_with_subsections.json
```

## Local test
From the folder containing these files and your JSON:
```
python3 -m http.server 8080
# then open http://localhost:8080/
```

—
Altitude House Consulting • Sanford LDR Search
