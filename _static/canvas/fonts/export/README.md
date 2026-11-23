# Figma export fallback fonts

These files are served at `/_static/canvas/fonts/export/` by the Canvas build's
public-asset copy rule. They are font-parser inputs for export; they do not change
the application's UI typography. Keep the adjacent SIL Open Font License notices.

- `inter-latin-400.woff`: Inter, Latin subset, regular weight. Source:
  https://cdn.jsdelivr.net/npm/@fontsource/inter@5.2.8/files/inter-latin-400-normal.woff
- `noto-sans-sc-400.ttf`: Noto Sans SC, regular weight, full font. Source:
  https://fonts.gstatic.com/s/notosanssc/v40/k3kCo84MPvpLmixcA63oeAL7Iqp5IZJF9bmaG9_FnYw.ttf
- `noto-sans-symbols.ttf`: Noto Sans Symbols, variable font with default weight 400,
  372,684 bytes. The export parser uses its default outlines for technical symbols
  such as `⌄`, `⌃` and `⌂` missing from both other fallbacks. Pinned source:
  https://github.com/google/fonts/blob/8b0a1d0f5983c89bc2b93f1b5fb55f9e252744b5/ofl/notosanssymbols/NotoSansSymbols%5Bwght%5D.ttf

The full CJK font is approximately 10 MB so the parser can obtain complete glyph
outlines without making requests to third-party font hosts. All three fonts are loaded
on demand and reused by FontManager. Do not replace them with WOFF2 without also
verifying the browser-side opentype parser supports the replacement format.
