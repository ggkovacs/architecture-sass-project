# Architecture for a [Sass](http://sass-lang.com) Project
Version: **1.1.0**

## Directory structure

    .
    ├── stylesheets/
    │   ├── base/
    │   └── ...
    │   ├── components/
    │   └── ...
    │   ├── globals/
    │   └── ...
    │   ├── layout/
    │   └── ...
    │   ├── vendors/
    │   └── ...
    │   └── main.{scss,sass}           # Primary Sass file (entry point)

### Base

The base/ folder holds what we might call the boilerplate stuff for your project. In there, you might find the reset (or Normalize.css, or whatever), probably some stuff dealing with typography, and, depending on the project, maybe some other files.

- `_reset.{scss,sass}` or `_normalize.{scss,sass}`
- `_typography.{scss,sass}`

### Components

For smaller components, there is the components/ folder (frequently called modules/). While layout/ is kind of macro (defining the global wireframe), components/ is more micro. It can contain all kinds of specific modules like a slider, a loader, a widget, or anything along those lines. There are usually a lot of files in components/ since your site is should be mostly composed of tiny modules.

- `_buttons.{scss,sass}`
- `_carousel.{scss,sass}`
- `_cover.{scss,sass}`
- `_dropdown.{scss,sass}`
- `_forms.{scss,sass}`
- `_thumbnails.{scss,sass}`
- `_icons.{scss,sass}`

### Globals

The globals/ folder (sometimes called utils/) gathers all Sass tools and helpers we’ll use across the project. Got a function? A mixin? Put it in there. This folder also contains a _variables.{scss,sass} file (sometimes _config.{scss,sass}) which holds all global variables for the project (for typography, color schemes, and so on).

- `_functions.{scss,sass}`
- `_helpers.{scss,sass}` or `_placeholders.{scss,sass}`
- `_mixins.{scss,sass}`
- `_variables.{scss,sass}` or `_config.{scss,sass}`
- `_media.{scss,sass}`

### Layout

The layout/ directory (sometimes called partials/) usually contains a number of files, each of them setting some styles for the main sections of the layout (header, footer, and so on). It also contains the _grid file which is the grid system used to build the layout.

- `_grid.{scss,sass}`
- `_header.{scss,sass}`
- `_footer.{scss,sass}`
- `_navigation.{scss,sass}`
- `_sidebar.{scss,sass}`

### Vendors

And last but not least, you will probably have a vendors/ folder containing all the CSS files from external libraries and frameworks – Bootstrap, jQueryUI, FancyCarouselSliderjQueryPowered, and so on. Putting those aside in the same folder is a good way to tell “Hey, this is not from me, not my code, not my responsibility”.

- `_bootstrap.{scss,sass}`
- `_jquery-ui.{scss,sass}`
- `_select2.{scss,sass}`

# License
MIT © 2016 Gergely Kovács (gg.kovacs@gmail.com)
