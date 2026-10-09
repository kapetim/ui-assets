# 🎨 assets

All-in-one place for **static, non-code assets** shared across the account's deployables — web pages, browser games, and native games.

Consumed as a **git submodule at `src/assets/`** (build-time) — and, optionally, referenced by tag-pinned URL where a repo publishes a static site.

## 🗂️ Layout

| Folder | What goes here |
| --- | --- |
| `src/img/` | images, sprites, icons, logos, textures |
| `src/audio/` | music / long-form audio |
| `src/sound/` | short sound effects |
| `src/fonts/` | webfonts and font files |
| `src/css/` | shared stylesheets and themes |
| `src/html/` | framework-agnostic HTML partials (meta, head, footers) |
| `src/tokens/` | design tokens (colors, typography, spacing) |

## 🚫 Not here

Application code, build logic, and data/content. Game data lives in `games`; site data in `data-science`; wiki/private content stays in their repos. This repo is **presentation only**.

## 🔗 Consumers

- [`games`](https://github.com/kapetim/games) — browser (Rust/wasm) and native (`windows`/`unix`) implementations — images · fonts · audio.
- [`data-science`](https://github.com/kapetim/data-science) — static Pages UI — html · css · images · tokens.
- [`browser-extensions`](https://github.com/kapetim/browser-extensions) — extension icons.

## 📦 Use it

```sh
git submodule add https://github.com/kapetim/assets.git src/assets
# or in an existing checkout
git submodule update --init --recursive
```

CI: check out with `submodules: recursive` (and `lfs: true` for large media).

## 📜 Licensing

Third-party assets and their licences are tracked in [`src/ASSETS-LICENSES.md`](src/ASSETS-LICENSES.md). Add an entry whenever you drop in an asset you did not create.
