# DevDocs for macOS

[![Release](https://img.shields.io/github/release/dteoh/devdocs-macos.svg)](https://github.com/dteoh/devdocs-macos/releases)
![Release Date](https://img.shields.io/github/release-date/dteoh/devdocs-macos.svg)

An unofficial [DevDocs API Documentation][1] viewer for macOS.

![App screenshot](./img/screenshot.png?raw=true "DevDocs for macOS screenshot")

## Features

- [x] Tabs
- [x] Global shortcut (<kbd>Option+Space</kbd>)
- [x] Automatic dark/light mode UI
- [x] Protocol handler integration (handle `devdocs-macos://` URLs)

### Protocol handler integration

Protocol handler integration allows you to control DevDocs through scripts. For
example:

```
$ osascript -e 'tell application "DevDocs" to open location "devdocs-macos://search?doc=rails&term=stro"'
```

... will tell DevDocs to open a new window and search the Rails documentation for
the term `stro`.

The app supports the following commands. When required parameters are not
supplied, the command is ignored.

#### `devdocs-macos://search`

This is for launching a search query in a new window.

| Query Parameter | Required | Description
| --------------- | -------- | -----------
| term            | Yes      | The search term, eg. `date`
| doc             | No       | Documentation scope, eg. `js`

#### `devdocs-macos://newWindow`

This opens a new window.

## Download & Install

Pre-built binaries can be downloaded from the [releases page][2].

Unzip, drag the app to Applications, and then run it.

### Homebrew

If you wish to install the application from Homebrew:

```
$ brew tap dteoh/devdocs
$ brew cask install devdocs-macos
```

The application will live at `/Applications/DevDocs.app`.

### Compatibility

The app is currently developed on Mojave and only support for Mojave can be
provided.

## License

```
DevDocs for macOS

Copyright (C) 2019 Douglas Teoh

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```

### App Icon

The app icon is a contribution courtesy of [@micck][3] ([#1][4]).


[1]: https://devdocs.io/
[2]: https://github.com/dteoh/devdocs-macos/releases
[3]: https://github.com/micck
[4]: https://github.com/dteoh/devdocs-macos/issues/1
