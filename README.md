CSS Social Media Buttons
==========================

A set of 48 social media buttons that can be added with just one HTML element, and come in two types (normal and flat) and in four styles (square, rounded, round, bordered). The icons are vector images meaning the buttons are scalable and retina proof.

## Installation ##

Simply put the CSS file in your project CSS folder and link to it in your `<head>` or copy/paste the content of the `dist/stylesheets/csmb.css` (or the minified file) into your own CSS file:

Not using all the buttons? Simply remove the buttons styling you won't use from the CSS file or compile your own CSS file that suits your needs with Gulp. Open `src/stylesheets/settings/_buttons.scss` and remove/comment out packages. Compile the SASS file with Gulp and add the resulting CSS to your project. 

You can also turn off button styles and/or types that you won't use, to keep the size of the CSS file small. This can be done by changing `true` to `false` for the various options in the file `src/stylesheets/csmb.scss`.


## How to use ##

Add an HTML element (`<a>`, `<span>` or `<button>`) with the class `csmb` or `csmb-flat`:

	<a href="#" class="csmb">CSS Social Media Button</a>
	<span class="csmb-flat">CSS Social Media Button</span>
	<button class="csmb">CSS Social Media Button</button>

Add a class of a (social) network, like for example `csmb-github` (see *'List of available buttons'* below for all the possibilities):

	<a href="#" class="csmb csmb-github">GitHub profile: username</a>
	<span class="csmb-flat csmb-github">GitHub profile: username</span>
	<button class="csmb csmb-github">GitHub profile: username</button>

However, this will only get you the base square buttons. You can extend the base styling with three styles: `csmb-border`, `csmb-rounded` and `csmb-round`. `csmb-border` can be combined with one of the other two styles.

	<a href="#" class="csmb csmb-border github">GitHub profile: username</a>
	<span class="csmb-flat csmb-rounded github">GitHub profile: username</span>
	<button class="csmb csmb-round csmb-border github">GitHub profile: username</button>

![](./demo/screenshot-2.png)

## List of available buttons ##

![](./demo/screenshot-1.png)


## Changelog v.3 ##

**v.3.0.0**

- Added SVG icons (instead of PNG) to make buttons scalable and sharp on higher pixel density screens
- Added 11 new buttons: `codepen`, `gitlab`, `invision`, `jsfiddle`, `medium`, `share`, `slack`, `snapchat`, `stackoverflow`, `steam` and `whatsapp`. 
- Added `csmb`-prefix to all classes to avoid issues with other styling.
- Added Gulp for asset compiling
- Added SCSS-Lint gem (using the SCSS guidelines as linter rules)
- Changed colour of buttons to match values from brand guidelines. All buttons are affected by this.
- Changed icons of buttons to match changes in brand (guidelines). Affected buttons: `deviantart`, `dropbox`, `github`, `google plus`, `instagram`, `issuu`, `myspace`, `paypal`, `reddit`, `tumblr`, `vine`.  
- Removed alternative buttons that didn't comply with brand guidelines. Affected buttons: `facebook alt`, `foursquare-alt`, `foursquare-alt alt`, `github-alt`, `instagram-alt`, `twitter alt`, `youtube-alt` and `youtube-alt alt`.
- Removed buttons without a distinct share or link purpose. Affected buttons: `chrome`, `drupal`, `firefox`, `git`, `ie`, `opera`, `safari`.
- Fixed difference in size of button types: `csmb-round` buttons were almost 8 pixels smaller than `csmb-border` buttons.

## Changelog v.2 ##

**[!]** = Can cause issues when updating from older version

**v.2.2.0**

- Added two new buttons: `foursquare` (the new "F" logo on a white background) and `swarm` (the bee on an orange background).
- **[!]** Renamed `foursquare` (the old "bouncing ball" logo) to `foursquare-alt`.
- **[!]** Renamed `foursquare.alt` to `foursquare-alt.alt`.
- **[!]** Renamed `github.alt` to `git`.
- Removed outline from buttons on `:hover`, `:focus` and `:active` states.
- Renamed the sprite image from `sprite-rsmb` to `icon-sprite`.

**v.2.1.0**

- Added five new buttons (browsers): `chome`, `safari`, `opera` (all three on white background), `firefox` (on light blue background) and `ie` (on blue background).
- Added darker inner border on the `:hover`, `:focus` and `:active` states of `.csmb-border` buttons.
- Changed colour of white buttons (for example: `flickr` and `github`) to `#F4F4F4`.
- Replaced absolute pixel values with percentage values for the `:after` and `:before` width and height properties.
- Replaced absolute pixel values with percentage values for the border-radius properties: 25% for `.csmb-rounded` and 50% for `.csmb-round`.
- Added a separate file for all SASS mixins + added mixins for vendor prefixed styling.

**v.2.0.0**

- Renamed `Round Social Media Buttons` to `CSS Social Media Buttons`: as it has become more than just round buttons.
- Moved all styling to just one file: *'One file to rule them all'*.
- Removed LESS version: LESS can't do everything SASS can, for example lists, which is essential for the *'One file to rule them all'* structure.
- Changed the way buttons are added: using lists (SASS version of arrays) instead of importing files. You can still remove/comment out the buttons you don't want to compile.
- Added variables to turn on/off certain button types and styles, making the compiled CSS smaller.
- Implemented "*rule*" that a button can only have one alternative button and that an alt button must be more than just a different colour (this was the case for `bitbucket`, `drupal` and `wordpress` for example). This has resulted in the removal of some alternative buttons: see *Removed buttons* section.
- **[Experimental]** Added extra style for `<button>` elements: this is turned off by default because some browsers (IE8 and Opera) seem to have difficulty with `:before` and `:after` on this element.

Button changes:

- Renamed `social-btn` to `csmb`.
- Added new button type: `csmb-flat`.
- Added three button styles: `csmb-border`, `csmb-rounded` and `csmb-round`.
- Added text-indent so you can add text for SEO/accessibility purposes within the element without it being shown.
- Moved icon from the `:after` layer to the base layer.
- Moved gradient from the base layer to the `:after` layer.
- Moved inset box-shadow from the `:after` layer to the base layer.
- Moved `:hover`, `:focus` and `:active` to only apply to anchor and button elements.

Added buttons:

- Added `blogger`: white icon on orange background.
- Added `delicious`: blue & black block on white background.
- Added `deviantart`: green rotated icon on brown-greyish background.
- Added `digg`: white icon on black background.
- Added `dropbox`: white icon on blue background.
- Added `grooveshark`: white icon on orange background.
- Added `paypal`: white favicon on dark blue background.
- Added `reddit`: alien head on light blue background.
- Added `soundcloud`: white icon on orange background.
- Added `spotify`: black sound waves on green background.
- Added `stumbleupon`: white icon on red background.

Removed buttons:

- Removed the default grey button style.
- Removed `bitbucket-alt`: the blue icon on white background.
- Removed `drupal-alt`: the white icon on blue background.
- Removed `github alt2`: the Octocat on white background.
- Removed `mail alt` button: the Gmail envelop icon on white background.
- Removed `pinterest-alt` button: the white icon on black background.
- Removed `skype alt` button: the 'S' without white border.
- Removed `wordpress alt` button: the white icon on grey background.
- Removed `youtube alt` button: the red play icon on white background.

Icon changes:

- Resized icons to be a bit smaller as to better fit the different types of buttons (especially the round without border buttons). Affected buttons: `bitbucket`, `facebook`, `github`, `github-alt` `instagram-alt`, `myspace`, `pinterest`, `tumblr`, `twitter-alt`, `vimeo`, `vine`, `wordpress`, `wordpress-alt` and `youtube-alt alt`.
- Removed light blue line from `facebook alt` button.
- Changed the `mail` icon: made the line narrower at the left and right side to make the illusion of an open envelope.
- Fixed positioning of `vimeo` and `vine` icon: they weren't in the middle of the button.
- Fixed icon of `github-alt`: the head of the octocat wasn't in the middle of the button anymore because of the resize.
- Fixed icon of `foursquare`: the white swoop stopped to early causing a empty space between the icon and the button borders (especially at square buttons).

Colour changes:

- Changed colour of buttons to match values from [Brandcolours.net](http://brandcolours.net/). Affected buttons: `facebook`, `foursquare`, `gplus`, `imdb`, `instagram-alt`, `lastfm`, `linkedin`, `path`, `pinterest`, `rss`, `skype`, `tumblr`, `vimeo`, `yelp` and `youtube-alt`.
- Changed colour of `wordpress` button from `#EBEBEB` (white) to `#21759B` (blue)
- Changed colour of white buttons (for example: `flickr` and `github`) to `#F8F8F8`.
- Changed colour of black buttons (for example: `github-alt` and `icheckmovies`) to `#383838`.
- Changed colour of `github` and `github alt` icons to `#383838`.

## Changelog v.1 ##

**[!]** = Can cause issues when updating from older version

**v.1.6.0**

- Added five new buttons: `bitbucket` (blue logo on white background), `bitbucket-alt` (white logo on blue background), `imdb`, `vine` and `yelp`.
- Changed icon of `gplus` button: larger icon.
- Changed icon of `mail alt` button: replaced with the Gmail favicon.
- **[!]** Removed `instagram-alt`: the small Instagram icon on a blue background.
- **[!]** Renamed `instagram-alt alt` to `instagram-alt`.

**v.1.5.3**

- Added alternative GitHub button: `github-alt`, a white Octocat on a black background (the current favicon).
- Added alternative YouTube button: `youtube-alt alt`, a white "play" icon on a red background (the current iPhone YouTube App icon).
- Changed colour of `youtube` icons from `#ED1C24` to `#CB2026`, making them a darker red.
- Changed colour of `youtube` button backgrounds from `#FC3F1A` to `#CB2026`, making them a darker red.
- **[!]** Removed second alternative E-mail button: `mail alt2`

**v.1.5.2**

- Added two alternatives for the E-mail button: `mail alt` (an envelope) and `mail alt2` (a '@').
- Changed background colour of all `mail` buttons from `#E3E9EC` to `#EBEBEB`.
- **[!]** Switched `instagram` and `instagram-alt` buttons, making the full icon version the primary button.
- **[!]** Renamed `instagram alt` to `instagram-alt alt`.
- Fixed positioning of `icheckmovies` icon: it wasn't in the middle of the button.

**v.1.5.1**

- Added a second alternative button for Instagram: `instagram-alt` (larger icon and brown border).
- **[!]** Switched `instagram-alt` and `instagram alt` in the sprite image.

**v.1.5.0**

- Added four new buttons: `pinterest` (on red background), `pinterest-alt` (on dark background), `instagram` and `instagram alt` (simplified icon made by [MarinaD](http://marinad.deviantart.com/art/FREE-Instagram-Vector-Icon-Logo-363269183)).
- Implemented a CSS transition on hover, changing the background colour smoothly.
- Added `:focus` to all buttons (only had `:hover`) and set `:hover, :focus & .active` correctly for default button style (it was changing `:before` and not the background of the base element).

**v.1.4.1**

- Improved positioning of Drupal icons
- Changed the pixel ratio from which the Retina sprite is used: from 2.0 to 1.5.

**v.1.4.0**

- Added six new buttons: `drupal` (official blue icon on white background), `drupal-alt` (white icon on blue background), `issuu`, `myspace`, `wordpress` (grey icon on white background) and `wordpress-alt` (white icon on grey background).

**v.1.3.1**

- **[!]** Changed the way how alternative buttons are used: instead of `github-alt` you'll have to use `github alt` (read more under the *Alternative buttons* section).
- **[!]** Switched Github icons: the favicon version is now the primary icon, the Octocat has become `github alt2`.

**v.1.3.0**

- Added four alternative buttons: `facebook-alt`, `foursquare-alt`, `github-alt2` and `youtube-alt2`.

**v.1.2.5**

- Fixed background-position for `youtube-alt` icon in SCSS file
- Removed inline-block mixin: is only needed for lower than IE8 browsers.
- Removed double background-size attribute in LESS file.

**v.1.2.4**

- Added browser prefix versions of the Retina media query & background-size, so that all browser use the Retina sprite if possible. 

**v.1.2.3**

- Added `content: ''` on `social-btn` to remove any content added to the button: resolves bug causing the button to break ([Issue #10](https://github.com/timhuisman/round-social-media-buttons/issues/10))
- Added `social-buttons.min.less` and `social-buttons.min.scss` for easier compiling of style into a minified and unminified version.

**v.1.2.2**

- **[!]** Updated `foursquare` button: changed background-colour and replaced the icon with its official (fav)icon: the green ball with white trail.

**v.1.2.1**

- Alphabetical order restored / Remove Trailing Whitespace (thanks [@cafferata](https://github.com/cafferata))
- Optimized images: Saved 2,6 KB of 11,1KB (thanks [@cafferata](https://github.com/cafferata))
- Added an alternative button: `skype-alt`.
- Repositioned both Skype icons to the right column in the sprites.
- **[!]** Switched Skype icons: the favicon version is now the primary icon.
- **[!]** Switched Github icons: the Octocat is now the primary icon.
- **[!]** Switched Twitter icons: the Twitter bird is now the primary icon.
- Changed colour of _"White"_ (actually `#F1F2F2`) icons to `#FFF`.
- Improved YouTube icons: the word 'Tube' has been made fully transparent.

**v.1.2.0**

- Added two new buttons: `skype` (thanks [@AMeijerNL](https://github.com/AMeijerNL)) and `icheckmovies`.
- Converted sprite from horizontally to vertically orientated (thanks [@AMeijerNL](https://github.com/AMeijerNL)), for smaller file size and load time.
- Added pointer cursor to button, so that non-anchor elements have the same visual button behaviour as anchor elements.
- Added source files for both normal and Retina sprites as Adobe Illustrator files.

**v.1.1.0**

- Added a SASS version (using the .scss notation) of the files

**v.1.0.1**

- Optimized sprites: removed 1px and 2px (Retina) empty space between icons and compressed the files to decrease filesize by almost 50%.
- Changed order of alternative icons in sprite: first the normal icon and then the alternative icon instead of vice versa.
