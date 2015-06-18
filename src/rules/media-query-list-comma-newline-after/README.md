# media-query-list-comma-newline-after

Require or disallow a newline after the commas of media query lists.

```css
    @media screen and (color), projection and (color) {}
/**                          ↑  
 *                These commas */
```

## Options

`string`: `"always"|"never"`

### `"always"`

There *must always* be a single newline after the comma.

The following patterns are considered warnings:

```css
@media screen and (color), projection and (color) {}
```

```css
@media screen and (color)
, projection and (color) {}
```

The following patterns are *not* considered warnings:

```css
@media screen and (color),
projection and (color) {}
```

```css
@media screen and (color)
,
projection and (color) {}
```

### `"never"`

There *must never* be whitepace after the comma.

The following patterns are considered warnings:

```css
@media screen and (color), projection and (color) {}
```

```css
@media screen and (color),
projection and (color) {}
```

The following patterns are *not* considered warnings:

```css
@media screen and (color),projection and (color) {}
```