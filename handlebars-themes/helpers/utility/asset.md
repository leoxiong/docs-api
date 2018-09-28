---
title: "asset"
keywords:
    - api
    - handlebars
    - themes
    - helpers
---

Usage: `{{asset "asset-path"}}`

### Description

The `{{asset}}` helper exists to take the pain out of asset management. Firstly, it ensures that the relative path to an asset is always correct, regardless of how Ghost is installed. So if Ghost is installed in a subdirectory, the paths to the files are still correct, without having to use absolute URLs.

Secondly, it allows assets to be cached. All assets are served with a `?v=#######` query string which currently changes when Ghost is restarted and ensures that assets can be cache busted when necessary.

Thirdly, it provides stability for theme developers so that as Ghost's asset handling and management evolves and matures, theme developers should not need to make further adjustments to their themes as long as they are using the asset helper.

Finally, it imposes a little bit of structure on themes by requiring an `assets` folder, meaning that Ghost knows where the assets are, and theme installing, switching live reloading will be easier in future.

### Examples

To use the `{{asset}}` helper to output the path for an asset, simply provide it with the path for the asset you want to load, relative to the `assets` folder.

For example:

```html
<link rel="stylesheet" type="text/css" href="{{asset "css/style.css"}}" />
<script type="text/javascript" src="{{asset "js/index.js"}}"></script>
<img src="{{asset "images/my-image.jpg"}}" />
```