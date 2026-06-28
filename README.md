# PortfoPlus Home — UI Replica

A static, mobile-first replica of the PortfoPlus home screen (`app.portfoplus.com/home`), built as pure HTML + CSS + inline SVG with one `<script>` block.

## What's included

- Header with notification badge
- Auto-rotating 3-slide banner (swipe-supported)
- Welcome line and editable KPI stats card (3 metrics + 4 quick actions)
- 生意工具 section: 筆單教室 strip + 4 tool cards
- 更多功能 grid (6 items, with COT and Ai badges)
- Floating 支援 button
- Bottom navigation with elevated home button
- Toast feedback on every interactive element
- KPI edit modal (Enter to save, Esc to cancel, click-outside dismiss)

## Device detection

The page detects device type before first paint and adapts the layout:

| Device | Trigger | Layout |
|---|---|---|
| Mobile | iPhone/Android UA or touch + <600px | Full-width app |
| Tablet | iPad UA or touch + 600–1023px | 540px-wide app, flanked background |
| Desktop | No touch + ≥1024px | 420px-wide app in dark phone-frame bezel |

Re-detects on resize and orientation change.

## Running locally

It's pure static HTML. Just open `index.html` directly in a browser:

```
file:///path/to/index.html
```

Or serve it:

```
npx serve -p 3000
```

## Status

This is a high-fidelity UI mockup of the home screen only. All interactive elements fire toast feedback; there's no backend, no real navigation between pages, and no data persistence across reloads.
