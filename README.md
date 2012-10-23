Gridlover Mixins
================

I built these mixing (currently just the Stylus mixin) to help generate CSS files inspired by Gridlover's tool to generate stylesheets that have typography with modular scale and vertical rhythm. These mixins only support the hard work Tuomas Jomppanen & Ville Vanninen have already done at (www.gridlover.net)[http://www.gridlover.net], be sure to check it out.

## Setup

Add the files to the top of your main stylesheet.

	@import 'config'
	@import 'rhythm'

Then update the values of `body-font-size`, `body-line-height`, `scale-factor` stored inside **config.styl** to your liking.

## Usage

	h1
		rhythm(4,1,2)

Now configure each typographical element to have vertical rhythm. Arguments should be passed through as scale, margin-before, margin-after. Please see the example stylesheet for a reference.

