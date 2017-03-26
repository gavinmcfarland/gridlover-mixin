Gridlover Mixin
===============

I built this mixin to help generate CSS files inspired by Gridlover's tool which lets you create typography with modular scale and vertical rhythm. These mixins only supplement the hard work Tuomas Jomppanen & Ville Vanninen have already done at [www.gridlover.net](http://www.gridlover.net), be sure to check it out.

## Setup

Add the following file to your main stylesheet.

	@import 'rhythm'

Then update values like `base-font-size`, `line-height-scale`, `scale-factor` stored inside the **config** file to your liking.

## Usage

Use the `rhythm()` mixin to set the vertical rhythm of each typographical element.

Arguments should be passed through as the font-size multiplier, margin-top multiplier, margin-bottom multiplier.

```stylus
rhythm: font-size [, margin-top, margin-bottom, line-height]
```

For example

```stylus
h1 {
	rhythm: 2, 1, 1
}
```

Outputs

```css
h1 {
  font-size: 36px;
  line-height: 48px;
  margin-top: 24px;
  margin-bottom: 24px;
}
```

### Custom line-height
By default the mixin calculates the appropriate line-height based on the computed font-size however if you wish to set this explicitly you can define it as the last argument in the mixin.

For example

```stylus
p {
	rhythm: 2, 1, 1, 4
}
```

## Configure

Change the default configuration for your project inside the **config** file.

```stylus
$unit = "px"
$base-font-size = 16px
$line-height-scale = 1.5
$scale-factor = 1.5
$true-scale = false
```
### Unit

Set which unit you would like the measurements to be output to. Choose from `"px"`, `"em"`, `"rem"`, or `"pxrem"`.

### Base font size

Set to the font size of your body copy. All typographical elements are calculated from this base font size.

### Line height scale

Set the scale for the vertical rhythm of your typography.

### Scale factor

Set the scale for the relationship of font sizes between each typographical element.

### True scale

Set to `true` if you would prefer the font size to be a direct multiple of the `font-size` multiplier.

## Changelog

### v1.4.0 (November 14th 2016)

- Refactored Stylus mixin
- Added support for, `em`, `rem`, `pxrem`
- Removed ouput of empty empty values
- Included the `$` character for valuble for easier identification
- Added `line-height` multiplier parameter to `rhythm()`
- Added `$true-scale` option to **config** file

### v1.3.0 (Jul 20, 2015)

- Added Bower support

### v1.2.0 (Aug 3, 2013)

- Added MIT License

### v1.1.0 (Jul 29, 2013)

- Added LESS support

### v1.0.0 (Oct 26, 2012)

- Stable version

### v0.1.0 (Oct 23, 2012)

- Initial commit

## Special thanks

Thanks for:

- [k9ordon](https://github.com/k9ordon) for adding LESS support
- [brunowego](https://github.com/brunowego) for adding Bower support

## License

This is licenced under the MIT License
