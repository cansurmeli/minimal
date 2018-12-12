# Minimal
Portfolio & blog theme powered by [Hugo](https://gohugo.io).

A fork of the original [minimal](https://github.com/calintat/minimal) theme developed by [Calin Tataru](https://github.com/calintat).

## Installation
You can install the theme either as a clone or submodule. The latter is recommended since it's a more modular approach and hence provides better management.

In order to install it as a submodule, from the root directory of your Hugo web site:
```
$ git submodule add https://gitlab.cansurmeli.com/can/minimal.git
$ git submodule init
$ git submodule update
```

Now you can get updates to Minimal in the future by updating the submodule:

```
$ git submodule update --remote themes/minimal
```

As the submodule is updated, it's recommended to commit that:

```
$ git add *
$ git commit -m "Submodule update."
```

## Configuration
After installation, take a look at the `exampleSite` folder inside `themes/minimal`.

To get started, copy the `config.toml` file inside `exampleSite` to the root of your Hugo site:

```
$ cp themes/minimal/exampleSite/config.toml .
```

Now edit this file and add your own information. Note that some fields can be omitted.

I recommend you use the theme's archetypes so now delete your site's `archetypes/default.md`.

## Features
You can tweak the look of the theme to suit your needs in a number of ways:

- The accent colour can be changed by using the `accent` field in `config.toml`.

- You can also change the background colour by using `backgroundColor`.

- Add colored 5px borders at the top and bottom of pages by setting `showBorder` to `true`.

For best results, I recommend you use a dark accent colour with a light background, for example:

```toml
[params]
    accent = "red"
    showBorder = true
    backgroundColor = "white"
```

### Fonts
The theme uses [Google Fonts](https://fonts.google.com) to load its font. To change the font:

```toml
[params]
    font = "Raleway" # should match the name on Google Fonts!
```

### Syntax highlighting
The theme supports syntax highlighting thanks to [highlight.js](https://highlightjs.org).

It's disabled by default, so you have to enable it by setting `highlight` to `true` in your config.

You can change the style used for the highlighting by using the `highlightStyle` field.

Only the "common" languages will be loaded by default. To load more, use `highlightLanguages`.

A list of all the available styles and languages can be found [here](https://highlightjs.org/static/demo/).

Please note the style and languages should be written in hyphen-separated lowercase, for example:

```toml
[params]
    highlight = true
    highlightStyle = "solarized-dark"
    highlightLanguages = ["go", "haskell", "kotlin", "scala", "swift"]
```
