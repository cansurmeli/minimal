# Minimal
Portfolio & blog theme powered by [Hugo](https://gohugo.io).

A fork of the original [minimal](https://github.com/calintat/minimal) theme developed by [Calin Tataru](https://github.com/calintat).

## Installation
You can install the theme either as a clone or submodule. The latter is highly recommended since it's a more modular approach and hence provides better management.

In order to install it as a submodule, from the root directory of your Hugo web site:
```
$ git submodule add https://gitlab.cansurmeli.com/can/minimal.git themes/minimal
$ git submodule init
$ git submodule update
```

Now you can get updates to Minimal in the future by updating the submodule:
```
$ git submodule update --remote themes/minimal
```

As the submodule is updated, it's recommended to separately commit that change by:
```
$ git add *
$ git commit -m "Submodule update."
```

## Configuration
After the installation, take a look at the `exampleSite` folder inside `themes/minimal`.

To get started, copy the `config.toml` file inside `exampleSite` to the root of your Hugo web site:
```
$ cp themes/minimal/exampleSite/config.toml .
```

Now edit this file and add your own information. Note that some fields can be omitted.

I recommend you use the theme's archetypes so now delete your site's archetypes.

```
$ rm archetypes/*
```

## Features
The original minimal theme manages some aspects of the design via the configuration file. However, I saw that it relates to a messy infrastructure. Also with the integration of [SASS](https://sass-lang.com), it's more modular.

Hence if you want to modify the appearance of the theme, you'll have to deal with either `assets/sass` or `layouts/partials/` folders mostly.

### Fonts
The theme uses [Google Fonts](https://fonts.google.com) to load it's font. To change the font, replace the content of the file on the location `assets/sass/dependencies/_google-fonts.css` with your Google Fonts'.

The original minimal theme goes with the option of configuring the font from `config.toml` file but with this approach(SASS infrastructure with Hugo's built-in asset bundling & minification) CSS content is much better managed.

### Syntax highlighting
The theme uses Hugo's built-in syntax highlighting; therefore no messy JS dependencies.

It's enabled by default, and you can customise it via the variables in `config.toml` under the `[params]` section.
