# USDM1 hero runtime

WebGL renderer for the USDM1 hero header art (hairline or thicker strokes, depth and cursor response). Configs are made in the M1 Hero Lab generator and exported as Webflow embeds.

## Use

Load a pinned version from jsDelivr:

```html
<div id="hero" style="position:absolute;inset:0;overflow:hidden;background:#121316"></div>
<script type="module">
import { createHero } from 'https://cdn.jsdelivr.net/gh/kwinton-26/usdm1-hero-runtime@v1.1.2/runtime/m1-hero.js';
createHero(document.getElementById('hero'), { concept: 'waves' });
</script>
```

Paste the config JSON from the generator in place of `{ concept: 'waves' }`.

## Versions

Always load a tagged version (`@v1.1.2`), never a branch, so published pages don't change when the runtime does. To release a change: update `runtime/m1-hero.js`, commit, tag a new version, then update the URL in the generator's hosted embed and in Webflow.

Three.js r169 loads from jsDelivr as a dependency.

## Changelog

- **v1.1.2:** new defaults: front stroke #D5E3F6 at 0.7 opacity, back stroke #8DADD3, legibility band 0.8.
- **v1.1.1:** vignette removed (always off, even in configs saved with one), and editing a config can no longer change the built-in defaults.
- **v1.1.0:** stroke width (`look.width`, 1 to 3, where 1 is the original hairline), corner radius for Ledger Bars (`params.radius`), transparent snapshots, and no scroll response.
- **v1.0.0:** first release.
