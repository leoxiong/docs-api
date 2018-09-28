---
title: "body_class"
keywords:
    - api
    - handlebars
    - themes
    - helpers
---

Usage: `{{body_class}}`

### Description

`{{body_class}}` – outputs dynamic CSS classes intended for the `<body>` tag in your `default.hbs` or other layout file, and is useful for targeting specific pages (or contexts) with styles.

The `{{body_class}}` helper outputs different classes on different pages, depending on what context the page belongs to. For example the home page will get the class `.home-template`, but a single post page would get `.post-template`.

Full details of what is output on each page can be found in the [context table](/docs/context-overview#section-context-table) on the [Context Overview](doc:context-overview) page.

### Examples

```html
<html>
    <head>...</head>
    <body class="{{body_class}}">
    ...
    {{{body}}}
    ...
    </body>
</html>
```
