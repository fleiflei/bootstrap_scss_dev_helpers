Bootstrap SCSS Development Helpers
==================================

Version: 1.0.0
Requires: Bootstrap SCSS v5+

Author: Florian Eickhorst
Author URI: https://github.com/fleiflei

License: GNU General Public License

Description: A collection of handy mixins and functions for development with Bootstrap SCSS.

## Helpers:

- Breakpoint indicator: show the current breakpoint in the upper left corner
- Grid overlay: shows the Bootstrap grid columns as an overlay (for non-fluid containers only)
- Manual indicators: mixin to highlight elements manually

## Setup

Require _bootstrap_scss_dev_helpers.scss in your SCSS after you include the Bootstrap's SCSS or at least Bootstraps _variables.scss. Be aware that it attaches to the element it is required inside. My best practice is to add it to the body element:

`body {
@include "bootstrap_scss_dev_helpers"
}
`

If possible I like to restrict this to my dev environment so none of the dev indicators will ever be shown in production. Inject your environment into your element and select it like this:

`body.env-development {
@include "bootstrap_scss_dev_helpers"
}
`
## Usage

### Breakpoint indicator

Enable the indicator by setting `$dev-enable-breakpoint-indicator: true;` before including _bootstrap_scss_dev_helpers.scss.

### Grid overlay

Enable the indicator by setting `$dev-enable-grid-view: true;` before including _bootstrap_scss_dev_helpers.scss.

By default the overlay is positioned like a non-fluid container. To show it for a fluid container set
`$dev-grid-overlay-fluid-container: true`

### Manual indicators

Sometimes I like to highlight the element I am working on to show its dimensions and positioning.

Enable the indicator by setting `$dev-enable-manual-indicators: true;` before including _bootstrap_scss_dev_helpers.scss.

Then simply include the mixin wherever you want:

`@include dmi();`
