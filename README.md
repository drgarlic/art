# art

## What is it ?

`art` is a theme generator that takes an image, generates colors from it and creates two themes from those colors, a dark and a light one.
It then updates your configuration files and any open terminal with the selected theme.
Each generated theme is saved in a special folder, that can be accessed at any time.

## How does it work ?

1. Load the image
2. Generate a certain number of colors
3. Choose 5 colors
    - The darkest
    - The redest
    - The greenest
    - The blueest
    - The lightest
4. Tweak those colors and create a grey color from the darkest one
5. Check colors
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
echo "PATH="${PATH}:`pwd`" >> ${HOME}/.bashrc
```

## How to use ?

```
usage: art [-h] [-a] [-c] [-d | -l | -s] [-i "file" "name" | -n "name" | -r | -u ["name"]] [-o] [-q]

art - Theme generator

Arguments:
(none)               Load the current theme
-h                   Show this help message and exit
-a                   Show a list of all available themes
-c                   Print the current theme
-d                   Load the dark version of the theme
-l                   Load the light version of the theme
-s                   Load the opposite version of the theme
-i "file" "name"     Create theme using an image
-n "name"            Load a specific theme
-r                   Load a random theme
-u [ "name" ]        Create a theme using a random image from unsplash,
                     the optional argument is a keyword to load specific images
-o                   Override an existing theme (used with -i
-q                   Quiet mode
```
