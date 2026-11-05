# USDM1 hero runtime

WebGL renderer for the USDM1 hero header art (hairline strokes, depth, cursor and scroll response). Configs are made in the M1 Hero Lab generator and exported as Webflow embeds.

## Use

Load a pinned version from jsDelivr:

```html
<div id="hero" style="position:absolute;inset:0;overflow:hidden;background:#121316"></div>
<script type="module">
import { createHero } from 'https://cdn.jsdelivr.net/gh/kwinton-26/usdm1-hero-runtime@v1.0.0/runtime/m1-hero.js';
createHero(document.getElementById('hero'), { concept: 'waves' });
</script>
```

Paste the config JSON from the generator in place of `{ concept: 'waves' }`.

## Versions

Always load a tagged version (`@v1.0.0`), never a branch, so published pages don't change when the runtime does. To release a change: update `runtime/m1-hero.js`, commit, tag a new version, then update the URL in the generator's hosted embed and in Webflow.

Three.js r169 loads from jsDelivr as a dependency.
