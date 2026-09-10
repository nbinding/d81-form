# D81 Form — Stead

A self-contained D81 financial preparation wizard, with automatic calculations, local browser storage, JSON import/export and a printable worksheet.

**Live calculator:** https://nbinding.github.io/d81-form/

Open `index.html` directly to use it offline. React, Three.js, Tailwind CSS, Base UI and the adapted shadcn button are embedded. Editable application sources are preserved inside the HTML in `stead-editable-source`.

## Display and accessibility

Use **Display** in the header to select text size (100–150%), the original font, plain sans-serif or the embedded OpenDyslexic font, and light, forest dark or device appearance. Optional number help writes amounts in words and explains conversions; maintenance explicitly identifies payments and receipts. Extra text spacing and reduced motion are also available.

Display preferences use `sessionStorage`: they survive refreshes in the current tab and reset when that tab’s session ends (browser session restoration may retain them). Financial answers continue to use separate local storage. OpenDyslexic font files and their SIL Open Font License are embedded in `index.html`.

## Branches and releases

- **Main** is the default, owner-controlled branch. Only the repository administrator can update it.
- **Public** is the GitHub Pages publishing branch. A push to `Public` rebuilds the live site from the repository root.
- Automatic merging is disabled. There is no automatic synchronisation between the branches.

After reviewing changes on Main, the owner can publish them manually:

```sh
git switch Main
git pull --ff-only origin Main
git switch Public
git pull --ff-only origin Public
git merge --ff-only Main
git push origin Public
git switch Main
```

If the branches have diverged, review and resolve the difference explicitly rather than force-pushing.

## Data and scope

Answers remain in the browser and are not sent to a backend. Browser storage and exported JSON backups are not encrypted. The attached source PDF and personal financial data are excluded from this repository.

The worksheet assists preparation of D81 (04.25); it does not replace the official signed form or consent order.
