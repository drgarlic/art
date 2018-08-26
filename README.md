# art

## Caution

**You will most likely have to edit the `EDITME` file since this script is at this moment only adapted for my dotfiles.**

## What is it ?

`art` is a theme generator that takes an image, generates colors from it and creates a theme with two variations from those colors, a dark and a light one.
It then updates some configuration files and any open terminal with desired colors.
Each generated theme is saved in a special folder, that can be accessed at any time.

## How does it work ?

1. Load an image
2. Generate a certain number of colors
3. Choose 5 colors
    - The darkest
    - The redest
    - The greenest
    - The blueest
    - The lightest
4. Tweak those colors and create a grey color from the darkest one
5. Check the colors
    - If some colors are too similar, adjust them
6. Generate files

## How to install ?

### Dependencies 

`imagemagick`: Used to generate the first array of colors

### Instructions

```
cd WHEREVER_YOU_WANT
git clone https://github.com/gawlk/art.git
cd art
echo "PATH="${PATH}:$( pwd )"" >> ${HOME}/.bashrc
```

## How to use ?

```
art - Theme generator

Arguments:
(none)                              Load the current theme
-blk                                Preset the black color
-blu                                Preset the blue color
-c | -copy "theme" "name"           Copy a theme and exit
-clear                              Clear all configuration files
-clear-all                          Clear all configuration files and delete the theme folder
-dark                               Set the brightness of the theme to dark
-delete "theme"                     Delete a theme and exit
-grn                                Preset the green color
-gry                                Preset the grey color
-h | -help                          Display this menu and exit
-i | -image "file" "name"           Create a theme using a local picture
-l | -link "link" "name"            Create a theme using a link to an image
-light                              Set the brightness of the theme to light
-list                               Display a list of available themes and exit
-n | -next                          Load the next theme from the list
-name                               Display the name of the current theme and exit
-o | -override                      Enable overriding of existing themes (one-time only)
-p | -previous                      Load the previous theme from the list
-q | -quiet                         Disable logs
-r | -random                        Select a random theme to load
-red                                Preset the red color
-reload                             Regenerate the configuration of the current theme (for devs)
-reload-all                         Regenerate the configuration of all the themes (for devs)
-s | -swap                          Swap the brightness of the current theme
-t | -theme "theme"                 Load a particular theme
-ua | -unsplash-artist "name"       Create a theme using a random picture from an Unsplash's artist
-uc | -unsplash-collection "name"   Create a theme using a random picture from an Unsplash's collection
-ud | -unsplash-daily               Create a theme using Unsplash's picture of the day
-ur | -unsplash-random              Create a theme using a random picture from Unsplash
-wht                                Preset the white color
```

## TODO

- Improve the selection of rgb in setters.rgb()
- Improve the ifs in checkers.colors()
- Find the perfect balance in tweakers.color()

## Contributors

- [turquoise-hexagon](https://github.com/turquoise-hexagon)
