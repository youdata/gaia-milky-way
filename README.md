# 银河全景 · The Milky Way as Gaia sees it

Two deep-zoom all-sky maps in galactic coordinates: the density of a 4,000,000-star random sample of Gaia DR3 (the Galaxy's shape and its dust) and every star brighter than G = 11, coloured by BP−RP; named objects placed from SIMBAD, a galactic grid, and a narrated tour that switches between the maps.

Live: https://youdata.github.io/gaia-milky-way/

The image pyramids are tile folders (`gaia-bright/`, `gaia-density/`: `header.idx` + `{z}/{x}/{y}.png`), so any static host serves them. Its fonts are in `fonts/`, trimmed to the page's characters. The narrated video is not included.

Data: ESA/Gaia/DPAC, Gaia DR3 (CC BY-SA 3.0 IGO); SIMBAD for the named objects.

## How it is made

From `infographic-examples/gaia-milky-way/build.mjs`, with rx (`~/rx-cli`):

```sh
rx export gaia-milky-way.json --out site --app /rx-graphic-editor/web/index.html --canvas --theme dark --lock-layers --tiles dir
rx publish site --to github:youdata/gaia-milky-way --yes
```
