# Sass-starter

[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/VeronQ/sass-starter/blob/master/LICENSE)
[![GitHub version](https://d25lcipzij17d.cloudfront.net/badge.svg?id=gh&type=6&v=1.0.0)](https://github.com/VeronQ/lipsum/releases)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/veronQ/sass-starter/graphs/commit-activity)

[Sass-starter](https://github.com/VeronQ/sass-starter) is a light and structured Sass-based architecture which can be used as a starter for any type of web project.  
This repository provides pre-configured styles, custom functions, useful mixins and a lot more to discover.

## Structure

Styles are divided into **7 folders** and exported in the same order into a [main](https://github.com/VeronQ/sass-starter/blob/master/main.scss) file.

1. [Abstracts](https://github.com/VeronQ/sass-starter/tree/master/abstracts)
2. [Base](https://github.com/VeronQ/sass-starter/tree/master/base)
3. [Components](https://github.com/VeronQ/sass-starter/tree/master/base)
4. [Layout](https://github.com/VeronQ/sass-starter/tree/master/layout)
5. [Pages](https://github.com/VeronQ/sass-starter/tree/master/pages)
6. [Themes](https://github.com/VeronQ/sass-starter/tree/master/themes)
7. [Vendor](https://github.com/VeronQ/sass-starter/tree/master/vendor)

## What's inside?

* Pre-configured colors, sizes, fonts and more
* Custom functions and mixins
* CSS debugger
* Utility classes and variables
* Normalize and base statements
* Usual files for starting a project

## Features

Here is a brief overview of what's inside this starter.

###### Colors variables
```sass
$white:        #ffffff;
$black:        #000000;

$gray-light:   mix($white, $black, 75%);
$gray:         mix($white, $black, 50%);
$gray-dark:    mix($white, $black, 25%);
```

###### Utility variables
```sass
$headings:     unquote('h1, h2, h3, h4, h5, h6');
$fields:       unquote('input, textarea, select');
$states:       unquote('&:hover, &:focus');
$medias:       unquote('img, video, iframe');
$all:          unquote('*, *:before, *:after');
```

###### Headings size
```sass
$headings-size: (
  h1: round($font-size-base * 2.25),
  h2: round($font-size-base * 2.00),
  h3: round($font-size-base * 1.75),
  h4: round($font-size-base * 1.50),
  h5: round($font-size-base * 1.25),
  h6: round($font-size-base * 1.00)
);
```

###### Z-index values
```sass
$z-index: (
  dropdown: 1010,
  sticky: 1020,
  modal: 1030,
  tooltip: 1040
);

@function z($key) {
  @return map-get($z-index, $key);
}
```

###### Asset helpers
```sass
@function asset($type, $file) {
  @return url($asset-base-path + '/' + $type + '/' + $file);
}

@function image($file) {
  @return asset('images', $file);
}

@function icon($file) {
  @return asset('icons', $file);
}

@function font($file) {
  @return asset('fonts', $file);
}
```

###### Shades of color
```sass
@function white($alpha) {
  @return rgba($white, ($alpha / 100%));
}

@function black($alpha) {
  @return rgba($black, ($alpha / 100%));
}

@function tint($color, $percent) {
  @return mix($white, $color, $percent);
}

@function shade($color, $percent) {
  @return mix($black, $color, $percent);
}
```

## Contributing

Feel free to contribute in order to improve this project.


## License
[MIT](https://github.com/VeronQ/sass-starter/blob/master/LICENSE)
