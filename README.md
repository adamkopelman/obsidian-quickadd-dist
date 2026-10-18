# QuickAdd 2.25.0 — release build for second-brain

> **This is not the official QuickAdd repository.** It holds the unmodified release files of
> **[QuickAdd](https://github.com/chhoumann/quickadd)** by Christian B. B. Houmann (chhoumann), MIT-licensed, so that
> [second-brain](https://github.com/adamkopelman/second-brain) can pin them as an optional git
> submodule at `.obsidian/plugins/quickadd`. For documentation (https://quickadd.obsidian.guide/docs/), support, bug reports
> and newer versions go to **[chhoumann/quickadd](https://github.com/chhoumann/quickadd)** — all credit belongs to its authors.

In second-brain, QuickAdd powers the clickable Actions row of `Dashboard.md`.

## Why this repo exists
Obsidian loads a community plugin from `main.js`, `manifest.json` and `styles.css` in
`<vault>/.obsidian/plugins/quickadd/`. Upstream keeps its sources in git and publishes those built
files only as release assets, so the upstream repository can't be used as that folder directly.
This repo contains exactly those three files from release [`2.25.0`](https://github.com/chhoumann/quickadd/releases/tag/2.25.0), byte for byte, plus
this README, upstream's license and ignore rules. Nothing was modified.

| File | sha256 |
| --- | --- |
| `main.js` | `4cab00f5170265ab511829aacf5fc8811e2ff7af8cc4ba088e1a16f83f001429` |
| `manifest.json` | `012617d4744a38464aeecb0d5f57180f547974e00282f20ea9d1c61ec3b8d1b6` |
| `styles.css` | `3915b3ad6319941a28bd7acfcc4ccaff74697ed561b7e99ca672fa0153c1c228` |

If QuickAdd saves you time, consider supporting its author: https://www.buymeacoffee.com/chhoumann

## Your settings stay local
Obsidian saves the plugin's settings to `data.json` in this folder; `.gitignore` ignores it and
everything else the plugin writes here, so your settings (including any API keys) are never
committed. second-brain's own settings for this plugin are not stored here: they live in the vault at
`.claude/skills/gtd-setup/scaffold/plugin-data/quickadd/data.json` and are copied into this
folder by `python .claude/skills/gtd-setup/apply.py .` (never over settings you already have).

## Alternative: install from Obsidian
Skip this submodule and install **QuickAdd** from Settings → Community plugins → Browse; Obsidian
puts it in the same folder.

## Updating
```sh
gh release download <tag> --repo chhoumann/quickadd --pattern main.js --pattern manifest.json --pattern styles.css --clobber
```
Update the version and hashes above, commit, and bump the submodule in second-brain.

## License
MIT — [`LICENSE`](LICENSE) is copied verbatim from
[chhoumann/quickadd at `2.25.0`](https://github.com/chhoumann/quickadd/blob/2.25.0/LICENSE) (Copyright (c) 2021 Christian Bager Bach Houmann).
