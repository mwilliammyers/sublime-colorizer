# colorizer

> A Sublime Text 2 & 3 plugin for changing the color of multiple words

The following configuration options are available:

- Regular Expression
- Case Sensitive
- Customize Colorize Colors
- Define "Always Colorizeed Keywords" with Customized Colors

## Usage

- Colorize: Select "Edit > Colorize Words > Colorize Words" and enter the words (separated by whitespace)
- Uncolorize: Select "Edit > Colorize Words > Uncolorize Words"
- Toggle Settings: Select "Edit > Colorize Words > Toggle Settings"
- Edit settings file: Select "Preferences" > "Package Settings" > "ColorizeWords", copy settings from default to user, and edit settings file. Available settings are:
- "colors_by_scope": Change the colorize colors.
- "permanent_colorize_keyword_color_mappings": Define always colorizeed keywords with specified colors, such as "TODO" or "FIXME". The optional "flag" parameter may be 0 (regex), 1 (literal), 2 (regex and ignore case) or 3 (literal and ignore case).
- Perl-style regular expression patterns are accepted. For example, to colorize "fix a bug" but not "prefix with", the expression could be "\\bfix .-\\b".

Note: These commands are also available in Command Panel with prefix "--ColorizeWords:--"

## How to find color scope

1. Select the text you want to find the scope for.
2. Tools > Developer > Show Scope Name (or ⌃⇧P)

- Paste this string inside color property:

```json
"permanent_colorize_keyword_color_mappings": [
    {
      "keyword": "FIXME",
      "color": "variable.parameter"
    }
]
```

*Color will change after you re-enter the tab*
