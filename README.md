# René — photo mosaic generator

Photo mosaic generator that runs entirely in the browser. No backend, no uploads: photos are read locally, tiled, matched and exported on the visitor's machine.

- Grid shapes: squares, bricks, hexagons, circles, diamonds, triangles, adaptive quadtree
- Overall masks: rectangle, circle, rounded, heart
- Flat tiles or scattered overlapping prints (rotation, overhang, drop shadow, white border)
- Tile colorization, color blend, repeat avoidance, random mirroring
- PNG / JPG export up to 8000 px wide

## Deploy

Static site, one file. Any static host works (Vercel, Netlify, Cloudflare Pages, GitHub Pages).

```
vercel        # or import the GitHub repo at vercel.com/new
```

Made by [eulst](https://eulst.fr).
