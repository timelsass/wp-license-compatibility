# wp-license-compatibility
License data for performing compatibility checks for WordPress Themes and Plugins

## Install

Install with yarn:

```
$ yarn add wp-license-compatibility
```

OR

Install with npm:

```
$ npm install wp-license-compatibility
```

## What is this?

Originally this data was gathered for supporting the WordPress Theme Review Team's [https://github.com/WPTRT/theme-sniffer](Theme Sniffer) [https://wordpress.org/plugins/theme-sniffer](Plugin), so that some validation could be done for theme submissions to WordPress.org's theme repository.  The data is useful outside of this context, and can be used for any purpose.

The data is indexed by SPDX license identifier, and includes the following:
- Accumulation of SPDX/non-SPDX license identifiers.
- Accumulation of various SPDX/non-SPDX license URIs.
- Accumulation of SPDX/non-SPDX names.
- Compatibility fields for `GPL-2.0-only`.
- Compatibility fields for `GPL-3.0-only`.

The initial support for compatibility checks was for checking against [https://github.com/WordPress/WordPress/blob/master/license.txt](WordPress.org's GPL-2.0-or-later license).  As the Theme Sniffer plugin progresses, we hope to add some compatibility checking to bundled resources in themes and perform some compatibility checking upon those.  This can lead to further data being added to support other licenses if the need arises.

As a note, while this repo uses various sources to accumulate the data - the license data does show favor towards the SPDX license identifiers.  SPDX is the most comprehesive and standardized approach to license expressions, which provides a solid base for extending.

## Roadmap

While gathering this data, most parts were scripted out, but manual inspection found various discrepencies.  The first stop on the roadmap is to flush out the scripting, and finalize a build process to keep the license data up to date with current revisions.

## Contributing

Pull requests are **definitely** welcome!

Until there's a proper build process in place for the base script, there's not any *strict limitations other than the JSON should be valid syntax and the overall structure shouldn't be modified extensively without further discussion*.  Do make sure to note references/urls as to why your PR should be included.  If for instance you add a new name to a license, where do you see it a lot, why should it be added, is it referenced in a particular package manager, a particular CMS, etc.  The more information there is, the better we can create a comprehensive list to cover different variations and needs!

## Special Thanks

The following resources have provided the data and insight used for this data:
- [https://spdx.org](SPDX)
- [https://github.com/spdx/license-list-data](SPDX/license-list-data)
- [https://www.gnu.org/licenses/license-list.en.html](FSF Compatibility Notes)
