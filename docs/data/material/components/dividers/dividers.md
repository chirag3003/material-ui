---
productId: material-ui
title: React Divider component
components: Divider
githubLabel: 'component: divider'
materialDesign: https://m2.material.io/components/dividers
---

# Divider

<p class="description">The Divider component provides a thin, unobtrusive line for grouping elements to reinforce visual hierarchy.</p>

{{"component": "modules/components/ComponentLinkHeader.js"}}

## Introduction

The Material UI Divider component renders as a dark gray `<hr>` by default, and features several useful props for quick style adjustments.

{{"demo": "IntroDivider.js", "bg": true}}

:::success
Use the handy `light` prop to make the Divider slightly lighter.
:::

## Basics

```jsx
import Divider from '@mui/material/Divider';
```

### Variants

The Divider component supports three variants: `fullWidth` (default), `inset`, and `middle`.

{{"demo": "DividerVariants.js", "bg": true}}

### Orientation

Use the `orientation` prop to change the Divider from horizontal to vertical.

{{"demo": "VerticalDividers.js", "bg": true}}

### Flex item

Use the `flexItem` prop to display the Divider when it's being used in a flex container.

{{"demo": "FlexDivider.js", "bg": true}}

### With children

Use the `textAlign` prop to align elements that are wrapped by the Divider.

{{"demo": "DividerText.js", "bg": true}}

## Customization

### Use with a List

When using the Divider to separate items in a List, use the `component` prop to render it as an `<li>`—otherwise it won't be a valid HTML element.

{{"demo": "ListDividers.js", "bg": true}}

### Icon grouping

The demo below shows how to combine the props `variant="middle"` and `orientation="vertical"`.

{{"demo": "VerticalDividerMiddle.js", "bg": true}}

## Accessibility

Due to its implicit role of `separator`, the Divider, which is a `<hr>` element, will be announced by screen readers as a "Horziontal Splitter" (or vertical, if you're using the `orientation` prop).

If you're using it as a purely stylistic element, we recommend setting `aria-hidden="true"` which will make screen readers bypass it.

```js
<Divider aria-hidden="true" />
```

If you're using the Divider to wrap other elements, such as text or chips, we recommend changing its rendered element to a plain `<div>` using the `component` prop, and setting `role="presentation"`.
This ensures that it's not announced by screen readers while still preserving the semantics of the elements inside it.

```js
<Divider component="div" role="presentation">
  <Typograph>Text element</Typography>
</Divider>
```

## Anatomy

The Divider component is composed of a root `<hr>`.

```html
<hr class="MuiDivider-root">
  <!-- Divider children goes here -->
</hr>
```

## Experimental APIs

### Material 3 Divider

The default Material UI Divider component follows the Material Design 2 specs.
To use the [Material 3](https://m3.material.io/) version, install the experimental `@mui/material-next` package.

```js
import Divider from '@mui/material-next/Divider';
```

{{"demo": "DividerMaterialYouPlayground.js", "hideToolbar": true, "bg": "playground"}}

To learn more about Material UI's MD3 implementation, visit the [Material 3 Components documentation](/material-ui/guides/material-3-components/).
