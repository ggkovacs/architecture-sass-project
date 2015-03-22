# Architecture for a [Sass](http://sass-lang.com) Project
Version: **1.0.0**

## Directory structure

    |-- scss/
    |   |-- base
    |   |   |-- _reset.scss         # Reset/normalize
    |   |   |-- _typography.scss    # Typography rules
    |   |   |-- ...                 # Etc.
    |   |
    |   |-- components or modules
    |   |   |-- _buttons.scss       # Buttons
    |   |   |-- _carousel.scss      # Carousel
    |   |   |-- _cover.scss         # Cover
    |   |   |-- _dropdown.scss      # Dropdown
    |   |   |-- _forms.scss         # Forms
    |   |   |-- ...                 # Etc.
    |   |
    |   |-- globals or utils
    |   |   |-- _functions.scss     # Sass functions
    |   |   |-- _helpers.scss       # Class & placeholders helpers
    |   |   |-- _mixins.scss        # Sass mixins
    |   |   |-- _variables.scss     # Sass variables
    |   |   |-- ...                 # Etc.
    |   |
    |   |-- layout
    |   |   |-- _footer.scss        # Footer
    |   |   |-- _grid.scss          # Grid
    |   |   |-- _header.scss        # Header
    |   |   |-- _navigation.scss    # Navigation
    |   |   |-- _sidebar.scss       # Sidebar
    |   |   |-- ...                 # Etc.
    |   |
    |   |-- widgets or sections or pages
    |   |   |-- _betslip.scss       # Betslip specific styles
    |   |   |-- ...                 # Etc.
    |   |
    |   |-- vendors
    |   |   |-- _bootstrap.scss     # Bootstrap
    |   |   |-- _jquery-ui.scss     # jQuery UI
    |   |   |-- ...                 # Etc.
    |
    |
    |-- main.scss                   # Primary Sass file (entry point)

### Base

The base/ folder holds what we might call the boilerplate stuff for your project. In there, you might find the reset (or Normalize.css, or whatever), probably some stuff dealing with typography, and, depending on the project, maybe some other files.

- `_reset.scss` or `_normalize.scss`
- `_typography.scss`

### Components or Modules

For smaller components, there is the components/ folder (frequently called modules/). While layout/ is kind of macro (defining the global wireframe), components/ is more micro. It can contain all kinds of specific modules like a slider, a loader, a widget, or anything along those lines. There are usually a lot of files in components/ since your site is should be mostly composed of tiny modules.

- `_buttons.scss`
- `_carousel.scss`
- `_cover.scss`
- `_dropdown.scss`
- `_forms.scss`
- `_thumbnails.scss`
- `_icons.scss`

### Globals or Utils

The globals/ folder (sometimes called utils/) gathers all Sass tools and helpers we’ll use across the project. Got a function? A mixin? Put it in there. This folder also contains a _variables.scss file (sometimes _config.scss) which holds all global variables for the project (for typography, color schemes, and so on).

- `_functions.scss`
- `_helpers.scss` or `_placeholders.scss`
- `_mixins.scss`
- `_variables.scss` or `_config.scss`
- `_media.scss`

### Layout or Partials

The layout/ directory (sometimes called partials/) usually contains a number of files, each of them setting some styles for the main sections of the layout (header, footer, and so on). It also contains the _grid file which is the grid system used to build the layout.

- `_grid.scss`
- `_header.scss`
- `_footer.scss`
- `_navigation.scss`
- `_sidebar.scss`

### Widgets or Sections or Pages

- `_betslip.scss`
- `_aside-links.scss`
- `_balance-info.scss`
- `_banner.scss`
- `_calendar-events.scss`

### Vendors

And last but not least, you will probably have a vendors/ folder containing all the CSS files from external libraries and frameworks – Bootstrap, jQueryUI, FancyCarouselSliderjQueryPowered, and so on. Putting those aside in the same folder is a good way to tell “Hey, this is not from me, not my code, not my responsibility”.

- `_bootstrap.scss`
- `_jquery-ui.scss`
- `_select2.scss`

# License
MIT © 2015 Gergely Kovács (gg.kovacs@gmail.com)
