# René · photo mosaic generator

Photo mosaic generator that runs entirely in the browser. No backend, no uploads: photos are read, matched and exported on the visitor's own machine. Fonts are embedded and the Content-Security-Policy blocks every network request, so nothing can leave the page.

- Grid shapes: squares, bricks, hexagons, circles, diamonds, triangles, adaptive quadtree
- Overall masks: rectangle, circle, rounded, heart
- Flat tiles or scattered overlapping prints (rotation, overhang, drop shadow, white border)
- Perceptual (Lab) tile matching, repeat avoidance, best-fit mirroring
- Full-resolution photos reloaded for large tiles; EXIF orientation respected
- Shuffle for a new arrangement with the same settings; cancellable renders
- PNG / JPG export up to 8000 px on the long edge
- Layered PSD export, written in the browser: every photo on its own transparent layer (rotation, border and shadow included), in stacking order inside a Photos group, whole tiles kept past the canvas edge. In After Effects use *Import as Composition – Retain Layer Sizes* to get one animatable layer per photo
- Optional smart objects: each photo is embedded once and every tile is an instance of it, so editing the photo updates all its copies. Cell shape, colorization, shadow and border stay live as vector masks and layer styles (PSD writing for this mode uses [ag-psd](https://github.com/Agamnentzar/ag-psd), MIT, bundled inline)

## Deploy

Static site, one file (`index.html`) plus `vercel.json` for security headers. Import the repo at vercel.com/new (framework: Other, no build command) or run `vercel`.

Made by [eulst](https://eulst.fr).
