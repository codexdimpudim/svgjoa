# joaosbreeze

An independently maintained fork of [breezeontop/svg](https://github.com/breezeontop/svg), operated by [codexdimpudim](https://github.com/codexdimpudim). The original Breeze app credits [x8rr](https://github.com/x8rr) and its other contributors/dependencies in Settings.

Primary site: https://cdn.jsdelivr.net/gh/codexdimpudim/svgjoa@main/index.svg

GitHub Pages entry address (redirects to the CDN version): https://codexdimpudim.github.io/svgjoa/

## Deployment

Publish from `main` → `/ (root)` in Settings → Pages → Deploy from a branch. `.nojekyll` is retained. No package installation or build is needed for this prebuilt snapshot. All entry-point assets remain relative so the `/svgjoa/` project path works.

`index.svg` is the interactive website, served through jsDelivr using its `/gh/user/repository@branch/file` format. `index.html` redirects visits on the GitHub Pages hostname to the CDN SVG and preserves the hash route. The redirect is hostname-limited so local HTML preview remains available. GitHub's SVG preview is an image preview and does not run the full website. About and license links use their rendered Pages/GitHub addresses because jsDelivr serves HTML files as plain text.

The CDN follows the public `main` branch. jsDelivr caches branches (normally up to 12 hours at its edge), so source edits can take time to appear. An exact commit URL may be used to verify a new revision immediately. See [jsDelivr GitHub and caching documentation](https://github.com/jsdelivr/jsdelivr#github).

To preview at the same subpath, serve the parent folder with `python3 -m http.server 4173` and open `/svgjoa/`.

## Changes dated 2026-10-27

- Owner-selected title and home heading: `joaosbreeze`. Existing layout, colors, settings keys and original credits retained.
- Removed Google Analytics and the remote error-monitor script from both entry points.
- Disabled the inherited click-triggered ad handler in `assets/app/index-BJFmwhbQ.js` and removed its ad destination.
- Removed the unrelated classroom loading screen. Disabled text substitution by default so labels retain ordinary readable characters; the original optional setting remains available.
- Added visible ownership, source, license and About links to both entry points, plus `about.html`.
- Preserved the upstream `LICENSE` unchanged.
- Use jsDelivr as the primary delivery origin, with a GitHub Pages redirect and preserved hash routes, so the inherited API origin allowlist supports media catalogs.

Snapshot received: `fd016fc129cf51c15735ca425d26ce54dc62d88f`. Keep this change notice and original notices when distributing modified versions.

## License and source limitations

The repository is licensed under [GNU AGPL-3.0](LICENSE). This fork retains that license and original credits. Modified files are marked with the date and nature of changes. The deployed site prominently links to this public repository and license. There is no warranty to the extent permitted by applicable law.

**Corresponding Source gap:** upstream provides bundled/minified JS and WebAssembly, but no original editable app source tree, dependency manifests or build scripts. Publishing these bundled files and fork modifications does not establish complete AGPL Corresponding Source compliance. Obtain the preferred editable source, dependency notices and build instructions for this exact snapshot from upstream before treating that requirement as resolved. Original third-party notices already present in the files are retained; fonts, media, games and dependencies can have additional terms.

## Service limitations

GitHub Pages serves static files. It cannot host the API or Wisp/WebSocket backend. The inherited `window.breezeConfig` pool in both entry points still points to upstream-operated external API/Wisp servers. Proxy browsing, movies/TV and manga depend on these services, their availability, CORS policies and content providers. Games load content from outside this repository. This fork does not operate or guarantee those services.

**Live verification on 2026-10-27:** The branded SVG, movie catalog and manga catalog load through jsDelivr. The inherited API returns `Access-Control-Allow-Origin: https://cdn.jsdelivr.net` for that origin, while it omits permission for the GitHub Pages origin. The Pages entry point therefore redirects to the CDN version. The homepage, game catalog/filtering and a proxied 2048 game were also verified on GitHub Pages, and a generic proxy destination loaded locally. Catalog loading does not establish that every external video stream, chapter or game will remain available. No new backend account or paid service was created.

The inherited analytics, error reporting and click ads are disabled in the active app. Other external requests (fonts, thumbnails, game/media content and API/proxy requests) remain part of the original functionality. See [About](about.html) for the visitor-facing explanation.

The owner selected the name `joaosbreeze` and requested the existing design be retained. The repository and URL remain `svgjoa`. No custom domain or paid hosting is configured. The upstream `robots.txt` still asks search engines not to index the site.
