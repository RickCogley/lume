# Migration from Lume v1 to Lume v2

## Added

- `includes` option to `module` and `mdx` plugins.

## Core

- Removed output extension detection in the filename: #430
- Removed `Page.dest` property #290.
  - This also removed `Page.updateDest` function.
- Removed `--dev` mode #244, #201.
  - Use the env variable `LUME_DRAFTS=true` to output draft pages.
- Renamed the interface method `Engine.renderSync` to `Engine.renderComponent`.
- Removed `site.includes()` function.
- Removed `Format.includesPath`.

## `search` Plugin

- Removed `returnPageData` option. Pages always return the `data` object
  https://github.com/lumeland/lume/issues/251
- Removed `search.tags()` function. Use `search.values("tags")`.
- Removed `data` filter.

## `toml` Plugin

- It's installed by default
- QUESTION: Should be possible to create pages from toml files?
  - No, use only for _data
  - Yes, but with a subextension to avoid conflicts with some configuration
    files like `netlify.toml`. For example: `page.tmpl.toml`.
  - Yes.

## `jsx` Plugin

- Removed `window.React` #332.

## `slugify_urls` Plugin

- Slugify static files by default. #447

## `netlify_cms` Plugin

- Renamed to `decap_cms`.

## `windi_css` Plugin

- Replaced with `unocss`.

## `markdown` Plugin

- Disable indented code blocks by default #376
- New option `useDefaultPlugins` that it's `true` by default.
- Removed `keepDefaultPlugins`

## `postcss` Plugin

- New option `useDefaultPlugins` that it's `true` by default.
- Removed `keepDefaultPlugins`

## `mdx` Plugin

- New option `useDefaultPlugins` that it's `true` by default.
- Removed `overrideDefaultPlugins`

## `remark` Plugin

- New option `useDefaultPlugins` that it's `true` by default.
- Removed `overrideDefaultPlugins`