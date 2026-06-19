# 復活 / FUKKATSU

**Print AR, resurrected.**

Fukkatsu is the AR-rescue platform from UNISEC. We replace dead, vendor-locked AR experiences (Adobe Aero, 8thWall trial expiries, abandoned native apps) with permanent, scan-via-camera, no-install-required digital experiences anchored to the same printed QR codes.

## Active rescues

| Client | Essay | Scenes | URL |
|---|---|---|---|
| Slant'd Magazine | *Hometown at Dusk* by Vicki Wang (Issue 06: Homecoming) | 5 | `slantd.secretmenu.sh/vicki` |

## How it works

1. **Reverse the dead URL.** Decode the original QR to get the dead vendor endpoint.
2. **Recover the media.** Original AR assets from client archives — video, image anchors, audio.
3. **Rebuild the destination.** Mobile-first static page, autoplay video or Ken-Burns still, branded to the publication.
4. **Print new QR.** Owned UNISEC URL that can never be deprecated.
5. **Side-by-side proof.** Old dead Aero QR vs new working Fukkatsu QR — same content, permanent.

## Stack

- Static HTML/CSS/JS — no framework, no build step
- Hosted on Vercel edge
- Domain pattern: `{client}.secretmenu.sh/{essay}/{scene}` per UNISEC domain canon
- Long-cache immutable media, short-cache HTML for hot-fixes

## Domain canon

- Client-facing pages always on a per-client subdomain of `secretmenu.sh`
- Platform brand home: `fukkatsu.app` (parked)
- `secretmenu.dev` / `chprcmnd.dev` are internal-only; never client-facing

## Repo layout

```
fukkatsu/
├── public/
│   ├── vicki/                 # Slant'd · Vicki Wang · Hometown at Dusk
│   │   ├── index.html         # scene picker
│   │   ├── *.html             # one file per scene
│   │   ├── shared.css         # mobile-first scene styling
│   │   └── media/             # mp4 + image anchors
│   └── index.html             # → redirects to /vicki (for now)
├── vercel.json
└── README.md
```

## License

Source code: TBD. Media assets are © Vicki Wang and used with permission via Slant'd Magazine.

---

UNISEC · Secret Menu LLC · 2026
