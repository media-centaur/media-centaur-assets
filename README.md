# Media Centarr — Assets

Heavyweight marketing artifacts (4K screenshots, banners, etc.) for the
[Media Centarr](https://github.com/media-centarr/media-centarr) project.

These are kept out of the main repo to avoid bloating clones and
rev-control history with multi-megabyte PNGs that change every release.
The main app repo still ships small web-resolution thumbnails inline;
this repo holds the click-through 4K versions referenced from the
README, marketing site, and wiki.

## Layout

```
screenshots/   4K supersampled PNGs (~3840px wide), lossless
```

## Serving

Assets are served via the [jsDelivr](https://www.jsdelivr.com/github) CDN.
Use URLs of the form:

```
https://cdn.jsdelivr.net/gh/media-centarr/media-centarr-assets@main/screenshots/<name>.png
```

jsDelivr caches with proper headers globally, no rate limit, no auth.
Avoid `raw.githubusercontent.com` — rate limited and not cached.

## Regenerating

Don't edit by hand. Run `scripts/regenerate-screenshots` in the main
[media-centarr](https://github.com/media-centarr/media-centarr) repo,
which writes web-resolution shots into the main repo and 4K versions
into this repo's `screenshots/` directory in one pass.
