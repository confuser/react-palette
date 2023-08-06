<p align="center">
  <h1 align="center">React Palette</h1>
</p>

<h3 align="center">
	Extract prominent colors from an image
</h3>

<p align="center">
  <a aria-label="Tests status" href="https://github.com/confuser/react-palette/actions/workflows/build.yaml">
    <img alt="" src="https://img.shields.io/github/actions/workflow/status/confuser/react-palette/build.yaml?label=Tests&style=for-the-badge&labelColor=000000">
  </a>
  <a aria-label="License" href="https://github.com/confuser/react-palette/blob/master/LICENSE">
    <img alt="" src="https://img.shields.io/github/license/confuser/react-palette?labelColor=000&style=for-the-badge">
  </a>
</p>

## Install
```
npm i @confuser/react-palette
```

## Usage
```jsx
import Palette from '@confuser/react-palette';
// In your render...
<Palette src={IMAGE_URL}>
  {({ data, loading, error }) => (
    <div style={{ color: data.vibrant }}>
      Text with the vibrant color
    </div>
  )}
</Palette>
```

```jsx
import { usePalette } from '@confuser/react-palette'

const { data, loading, error } = usePalette(IMAGE_URL)

<div style={{ color: data.vibrant }}>
  Text with the vibrant color
</div>
```

## Palette callback example
```js
{
  darkMuted: "#2a324b"
  darkVibrant: "#0e7a4b"
  lightMuted: "#9cceb7"
  lightVibrant: "#a4d4bc"
  muted: "#64aa8a"
  vibrant: "#b4d43c"
}
```

## Notes

That library was created using `node-vibrant` to extract the prominent colors.

[https://github.com/akfish/node-vibrant](https://github.com/akfish/node-vibrant)
