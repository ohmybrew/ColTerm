# ColTerm

**Forked from: [@SeungheonOh/ColTerm](https://github.com/SeungheonOh/ColTerm/)**

*Changes include: Modifications to flags, support for my custom Xresources scheme*.

---

Simper, more Unix-philosophical implementation of auto colorscheme generator. It gets Image as an input, gives you a well generated color scheme.

## Things

![ColTerm](https://github.com/SeungheonOh/ColTerm/blob/master/img/colterm.ong)

Well, as you notice, it's really similar to [pywal](https://github.com/dylanaraps/pywal). Unlike pywal, colterm is designed make a colorscheme only,
but not to manage whole wallpaper system, therefore it's a lot simpler. You might ask, then why should I use it? I would say colterm would work best for those of you 
who would save your colorschemes by a image instead of having not really clean or commented clusters of colorschemes in you config files. You can just
save a file with bunch of image links that you like, and use colterm to got a colorscheme without any dirty work of copying/finding/uncommenting
colorschemes.

It supports only Xresources. However, you can input a ```Tamplate``` for your config with placesholders (like ```background``` or ```color1```) to generate any kinds of configs.

## Requirements

Nope, only Go standard libraries (I wrote the coloring algorithm by myself, compactly). You need ```xrdb``` to set Xresources however.

## Usage

```sh
USAGE:
   colterm <OPTIONS> <FILE/URL>
OPTIONS:
  -bg int
        Set background brightness(0 - 255) (default 20)
  -sn string
        The scheme name to give, will be part of the export(ex) path
  -ex string
        Export file to (Path) (default ~/.xres/themes/(sn))
  -f string
        Input file, use this option or put file behind the options
  -fg int
        Set foreground brightness(0 - 255) (default 150)
  -po  bool
        Print colors only without applying to Xresources (default true)
```

## Binary Building

`go build -o colterm .`
