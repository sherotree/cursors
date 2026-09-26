# @sherotree/cursors

Reusable **SVG hotspot cursors** for the web: default, pointer, grab, and grabbing — plus slightly smaller variants under `1280px` viewport width.

Originally extracted from [Uwarp](https://www.uwarp.design) design tools.

![@sherotree/cursors demo](https://cdn.jsdelivr.net/npm/@sherotree/cursors@0.1.1/media/demo.gif)

## Install

```bash
npm install @sherotree/cursors
# or
pnpm add @sherotree/cursors
yarn add @sherotree/cursors
```

## Usage

### Global (site-wide)

```js
import '@sherotree/cursors/style.css'
```

In Next.js App Router, import once from `app/layout.tsx` (or your root layout).

This sets `body` cursors and remaps common interactive selectors (`a:hover`, `button:hover`, `[role=button]`, etc.). It also overrides Tailwind utilities `.cursor-default`, `.cursor-pointer`, `.cursor-grab`, and `.cursor-grabbing` so those keep the custom look.

### Scoped (subtree only)

```js
import '@sherotree/cursors/scoped.css'
```

```html
<div class="sherotree-cursors">
  <!-- custom cursors apply inside here -->
</div>
```

## What’s included

| Cursor | Classes / triggers |
| --- | --- |
| Default | `body`, `.cursor-default` |
| Pointer | links/buttons hover, `.cursor-pointer` |
| Grab | `.cursor-grab`, inline `cursor: grab` |
| Grabbing | `.cursor-grabbing`, inline `cursor: grabbing` |

Assets live under `assets/*.svg` with correct hotspot offsets baked into the CSS `url(...) x y` values.

## License

MIT © Sherotree

Visual treatment inspired by [maximatherapy.com](https://maximatherapy.com). Confirm you have rights to redistribute any derived artwork before publishing forks with different assets.
