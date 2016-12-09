# 64tass Bundle for TextMate 2

If you like to code for Commodore 64 and love TextMate (*works with current version,
not tested via TextMate1*), you’ll enjoy this bundle. [64tass][64tass] is cross 
assembler targeting the **65xx** series of micro processors.

Just type your code and hit `⌘` + `R`

## Installation

    cd ~/Library/Application Support/TextMate/Bundles/
    git clone https://github.com/vigo/textmate2-64tass-bundle.git "64tass Bundle.tmbundle"
    # relaunch textmate

## Todo

* Syntax highlighting and language grammar is work-in-progress now!

## Requirements

* [MacVICE][macvice] or [VICE][vice]
* [64tass compiler][64tass_home] homepage.

[64tass]:          http://singularcrew.hu/64tass/
[macvice]:         http://lallafa.de/blog/c64-projects/macvice/
[vice]:            http://vice-emu.sourceforge.net/macosx.html
[64tass_home]:     http://tass64.sourceforge.net/

## TextMate Setup

You need to set your environment variables. We have two required and two
optional variables.

### Required Variables

#### `TM_64TASS_PATH`

Binary file location of 64tass executable. You can put this executable
under your global path such as `/bin/64tass` or wherever it’s placed. 
Example: `/Users/vigo/bin/64tass`.

#### `TM_VICE_PATH`

Command-line binary of X64.app. Vice comes with these tools under `tools/`
folder:

    c1541
    cartconv
    petcat
    vice-launcher.sh
    x128
    x64
    x64dtv
    x64sc
    xcbm2
    xcbm5x0
    xpet
    xplus4
    xvic

Example: `/Users/vigo/Applications/MacVice/tools/x64`

### Required Variables

#### `TM_64TASS_OPTIONS`

Default options are: `-C -a`. You can override it via setting `TM_64TASS_OPTIONS`
variable. You can check the available options for 64tass via `64tass --help`

#### `TM_VICE_OPTIONS`

You can define extra options for `x64` executable. Try: `x64 -h` for all
options. I’m using `+card` which is **Disable default cartridge** in my
configurations. It’s totally up to you.

## Screens

![Example code snippet](Screens/tass-code.png "Example code snippet")

![Example runner output](Screens/tass-runner.png "Example runner output")

Output theme can be vary according to your preferences.

## Contributer(s)

* [Uğur "vigo" Özyılmazel](https://github.com/vigo) - Creator, maintainer

## Contribute

All PR’s are welcome!

1. `fork` (https://github.com/vigo/textmate2-64tass-bundle.git)
1. Create your `branch` (`git checkout -b my-features`)
1. `commit` yours (`git commit -am 'added killer options'`)
1. `push` your `branch` (`git push origin my-features`)
1. Than create a new **Pull Request**!

## License

This project is licensed under MIT