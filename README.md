# Serpent Robotics — Homepage

Static, self-contained homepage. No build step, no dependencies. All real brand
assets are pulled directly from the `Content/` folder.

## Files
- `index.html` — page markup / all copy
- `styles.css` — all styling (brand colors live in the `:root` block at the top)
- `main.js` — mobile nav toggle + footer year
- `Content/` — brand assets (images, logo, icons, video, colors) — source of truth

## Preview
Open `index.html` in a browser, or run a local server (better for the video + paths):

```powershell
# from this folder
python -m http.server 8000    # then visit http://localhost:8000
```

## Brand tokens (from Content/Colors/Frame 103.png)
| Token | Hex | Use |
|---|---|---|
| Orange | `#FF4A00` | accent, buttons, marks |
| Dark brown | `#1F0A00` | page background |
| Near-black | `#110601` | alternating sections |
| Off-white | `#F4EFEC` | text |
| Muted brown | `#4A382F` | — |

## Where each asset is used
| Section | Asset |
|---|---|
| Header / footer logo | `Content/Logo/Horizontal_White.svg` |
| Hero background | `lucakuancao_..._looking_straight_up_..._1 1.png` |
| Product render | `Content/Images/ProductVisual.png` |
| Step 1 – Identify | `Content/Images/image 39.png` |
| Step 2 – Ascend | `Content/Images/PeterPhoto 1.png` |
| Step 3 – Cut | `Content/Images/ADT05003 1.png` |
| Mission background | `lucakuancao_..._wide_top-down_..._1 1.png` (power-line corridor) |
| How It Works video | `Content/Video/SerpentWebsiteVideo.mp4` (poster: ADT05003) |
| Benefits image | `Content/Images/image 39.png` |
| CTA background | `lucakuancao_..._top-down_view_..._3 1.png` |
| Footer contact icons | inline SVG (recolored to brand orange) |

## Notes / things you may want to change
- **Video is 150 MB.** It's embedded as click-to-play (`preload="none"`) so it only
  downloads when a visitor presses play — never on page load. If you host this
  publicly, consider compressing it or using a streaming host (YouTube/Vimeo/Mux).
- **Capability & step icon SVGs** (`Content/Icons/*.svg`) are 90–190 KB pre-composed
  raster cards, so the page uses live HTML text with orange marks instead (faster,
  better for SEO/accessibility). Swap them in if you prefer the designed icons.
- **Team headshots** (`2025-11-4_VentureLab_Serpent-15/21/26`) aren't placed yet —
  they're a good fit for a future "Company / Team" section or page.
- The two `Screenshot ... .png` controller UI images aren't placed yet either — a
  natural fit for the "Communicating" capability if you want to show the interface.
- Testimonials are text-only (no headshots available for the external arborists).
