# fluentui-system-icons-font
Manually created fonts of the
[FluentUI System Icons](https://github.com/microsoft/fluentui-system-icons)
([MIT License](https://github.com/microsoft/fluentui-system-icons/blob/master/LICENSE)).

## Provided fonts
- `FluentUI Filled Color`
- `FluentUI Filled Monochrome`
- `FluentUI Regular Color`
- `FluentUI Regular Monochrome`

## Manual creation process
### Get resources
1. Download latest release from https://github.com/microsoft/fluentui-system-icons
2. Download latest release from https://github.com/EnnoxHD/fluentui-system-icons-extractor
    - edit `src/main/java/com/github/ennoxhd/fluentui/extractor/app/FluentUiResources.java`
        - change `resources` variable
        - change `output` variable if needed
    - use command `gradlew run` in the root folder of `fluentui-system-icons-extractor`

### Generate fonts
The following description will lead to the generation of **4 fonts** in total:
- `FluentUI Filled Color`
- `FluentUI Filled Monochrome`
- `FluentUI Regular Color`
- `FluentUI Regular Monochrome`

1. Go to https://icomoon.io/app/#/projects
2. `New project`: `FluentUI System Icons`
3. `Import Icons`: Select all svg files of type **[filled / regular]**
4. Hamburger menu icon: `Select all icons`
5. Color Palette:
    - **color**: skip this
    - **monochrome**: `Color Themes -> Delete`
6. `Generate Font`
7. `Preferences`:
      - `Font Name`:
        - `FluentUI Filled Color`
        - `FluentUI Filled Monochrome`
        - `FluentUI Regular Color`
        - `FluentUI Regular Monochrome`
    - `Class Prefix`:
        - `flt-fc-`
        - `flt-fm-`
        - `flt-rc-`
        - `flt-rm-`
    - `Metadata`:
      - `URL`: `https://github.com/EnnoxHD/fluentui-system-icons-font`
      - `Description`: `Fluent System Icons are a collection of familiar,
        friendly and modern icons from Microsoft.`
      - `Copyright`: `Copyright (c) 2020 EnnoxHD`
      - `Designer`: `Microsoft Corporation`
      - `Designer's URL`: `https://github.com/microsoft/fluentui-system-icons`
      - `License`: `MIT License`
      - `License URL`: `https://github.com/EnnoxHD/fluentui-system-icons-font/blob/master/LICENSE`
    - `Version`:
      - `Major`: `1` (according to the current release)
      - `Minor`: `1` (according to the current release)
8. `Reset -> Reset Codes`: `e000`, `Reset Codes`
9. `Download`
10. Copy the contents of the `zip` files to their appropriate location
    - `FluentUI System Icons Filled Color`: `fluentui-system-icons-font/fonts/color/filled`
    - `FluentUI System Icons Filled Monochrome`: `fluentui-system-icons-font/fonts/monochrome/filled`
    - `FluentUI System Icons Regular Color`: `fluentui-system-icons-font/fonts/color/regular`
    - `FluentUI System Icons Regular Monochrome`: `fluentui-system-icons-font/fonts/monochrome/regular`

### Release
The release gets a tag name consisting of the current
[FluentUI System Icons](https://github.com/microsoft/fluentui-system-icons)
release name with `major.minor.patch` (e.g. `1.1.43`) followed by
a `pre-release label` counting from 1 (e.g. `-1`) for each release of the same
[FluentUI System Icons](https://github.com/microsoft/fluentui-system-icons)
version in this repository.

Then this will follow the ordering rules defined by [Semantic Versioning](https://semver.org/).

**Example releases in order**
- `1.1.43-1`
- `1.1.43-2`
- `1.1.43-3`
- `1.1.44-1`
- `1.2.0-1`
