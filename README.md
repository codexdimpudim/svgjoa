# svgjoa

An independently maintained fork of [breezeontop/svg](https://github.com/breezeontop/svg), operated by [codexdimpudim](https://github.com/codexdimpudim). The original Breeze app credits [x8rr](https://github.com/x8rr) and its other contributors/dependencies in Settings.

Site: https://codexdimpudim.github.io/svgjoa/

## Deployment

Publish from `main` → `/ (root)` in Settings → Pages → Deploy from a branch. `.nojekyll` is retained. No package installation or build is needed for this prebuilt snapshot. All entry-point assets remain relative so the `/svgjoa/` project path works.

`index.html` is the normal website. `index.svg` is an alternate SVG entry point with the same fork notices. Use the Pages URL for normal browsing; GitHub's SVG preview is an image preview and does not run the full website.

To preview at the same subpath, serve the parent folder with `python3 -m http.server 4173` and open `/svgjoa/`.

## Changes dated 2026-10-27

- Provisional title and home heading: `svgjoa`. Existing layout, colors, settings keys and original credits retained.
- Removed Google Analytics and the remote error-monitor script from both entry points.
- Disabled the inherited click-triggered ad handler in `assets/app/index-BJFmwhbQ.js` and removed its ad destination.
- Removed the unrelated classroom loading screen. Disabled text substitution by default so labels retain ordinary readable characters; the original optional setting remains available.
- Added visible ownership, source, license and About links to both entry points, plus `about.html`.
- Preserved the upstream `LICENSE` unchanged.

Snapshot received: `fd016fc129cf51c15735ca425d26ce54dc62d88f`. Keep this change notice and original notices when distributing modified versions.

## License and source limitations

The repository is licensed under [GNU AGPL-3.0](LICENSE). This fork retains that license and original credits. Modified files are marked with the date and nature of changes. The deployed site prominently links to this public repository and license. There is no warranty to the extent permitted by applicable law.

**Corresponding Source gap:** upstream provides bundled/minified JS and WebAssembly, but no original editable app source tree, dependency manifests or build scripts. Publishing these bundled files and fork modifications does not establish complete AGPL Corresponding Source compliance. Obtain the preferred editable source, dependency notices and build instructions for this exact snapshot from upstream before treating that requirement as resolved. Original third-party notices already present in the files are retained; fonts, media, games and dependencies can have additional terms.

## Service limitations

GitHub Pages serves static files. It cannot host the API or Wisp/WebSocket backend. The inherited `window.breezeConfig` pool in both entry points still points to upstream-operated external API/Wisp servers. Proxy browsing, movies/TV and manga depend on these services, their availability, CORS policies and content providers. Games load content from outside this repository. This fork does not operate or guarantee those services.

The inherited analytics, error reporting and click ads are disabled in the active app. Other external requests (fonts, thumbnails, game/media content and API/proxy requests) remain part of the original functionality. See [About](about.html) for the visitor-facing explanation.

Branding is provisional pending the owner's preferred site name and design. No custom domain or paid hosting is configured. The upstream `robots.txt` still asks search engines not to index the site.
