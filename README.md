<h1 align="center">
<b>@antv/smart-color</b>
</h1>

<div align="center">
A JavaScript library for color computation.
</div>

## ✨ Features

* **Palette Generation**: Automatic generation of continuous or categorical palette based on [color scheme](https://github.com/neoddish/color-palette-json-schema#colorschemetype).
* **Palette Optimization**: Automatic palette optimization enables colors in the palette to be distinguished more easily.
* **Color Simulation**: Simulation of color in color blind and gray scale.
* **Professional Test**: Provide professional methods to color testing.
* **Get Palette**: Get palettes from strings and images.

## 📦 Installation

```bash
$ npm install @antv/smart-color
```

## 🔨 Getting Started

* Palette Generation

```ts
import { paletteGeneration } from '@antv/smart-color';

paletteGeneration("monochromatic", {
  color: {
    model: "rgb",
    value: { r: 91, g: 143, b: 249 },
  },
  count: 7,
  tendency: "shade"
});
```

<div align="center">
  <img src="https://gw.alipayobjects.com/zos/antfincdn/vmwgZKfSZB/jieping2021-07-01%252520xiawu3.01.26.png" alt="auto generated palette">
</div>

* Palette Optimization

```ts
import { PaletteOptimization } from '@antv/smart-color';

const palette = {
  name: "color4",
  semantic: null,
  type: "categorical",
  colors: [
    { model: "rgb", value: { r: 101, g: 120, b: 155 }, },
    { model: "rgb", value: { r: 91, g: 143, b: 249 }, },
    { model: "rgb", value: { r: 97, g: 221, b: 170 }, },
    { model: "rgb", value: { r: 246, g: 189, b: 22 }, }
  ],
}
paletteOptimization(palette, {
  locked: [true],
  simulationType: "grayScale"
});
```

<div align="center">
  <div>
    <span>Before:</span>
    <img src="https://gw.alipayobjects.com/zos/antfincdn/jT0dtYywS8/jieping2021-07-01%252520xiawu3.24.42.png" alt="palette before optimization">
  </div>
  <div>
    After:
    <img src="https://gw.alipayobjects.com/zos/antfincdn/HCdz8Z8kr%26/jieping2021-07-01%252520xiawu3.24.29.png" alt="palette after optimization" >
  </div>
</div>

* Color Simulation

```ts
import { colorSimulation } from '@antv/smart-color';

const color = {
  model: "rgb",
  value: { r: 91, g: 143, b: 249 },
}
colorSimulation(color, "achromatomaly");
```

<div align="center">
  <img height=100 src="https://gw.alipayobjects.com/zos/antfincdn/fxjnaPrLZ6/jieping2021-07-01%252520xiawu3.11.52.png" alt="color simulation result">
</div>

## 🔗 Links

* [API Reference](./docs/api/readme.md)

## License

MIT
