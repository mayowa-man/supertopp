# SUPER TOPP — lighter build

This version keeps the existing design/content but makes the site lighter visually and in the browser.

Changes:
- Converted raster assets in `src/images` from PNG/JPEG to WebP, reducing the image payload substantially.
- Reduced hero height, typography scale, section padding, card padding, and navigation height.
- Simplified page-transition animation.
- Removed the GSAP/Lenis runtime code from `App.tsx` (dependencies remain in package.json/package-lock so the lockfile stays untouched).
- Reduced the animated water-particle canvas from potentially hundreds of particles to a capped, simpler particle effect.
- Kept the existing pages, routes, and branding.

Important:
- The original ZIP included a `.git` directory; this optimized ZIP intentionally does not.
- Run `npm install` and then `npm run build` before deploying.
- If you want the maximum bundle reduction, the next pass can remove unused packages from `package.json` and regenerate the lockfile.
