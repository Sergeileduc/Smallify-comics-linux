# Smallify-comics

## Requirements
smallifiy uses Image Magick, please install first
`sudo apt-get install imagemagick`

for CBR files, you'll need rar and unrar:

`sudo apt install rar unrar`

smallify-recurse is a Python3 script (you need Python3)

## Install
Put files into a known folder of your PATH (exemple : `.local/bin`)
or make links (ln) between your git clone folder files, and your path `.local/bin`

Make sure they have execution (x) permission

(if not, `chmod +x filename`)

## Use

### Only in current folder
In a folder containing multiple cbr and/or cbz files,

open a Terminal and type :

`smallify-all`
This will smallify all comics and saves in "Smaller_comics" default folder
Safe to use.

`smallify-all -f "My low bandwith comics`

`smallify-all --folder "My low bandwith comics`

This will create `My low bandwith comics` folder and store smallified comics inside.
Safe to use

`smallify-all -r`

`smallify-all --replace`

This will REPLACE your original comics !! BE CAREFUL !

JPEG quality and image height can be specified with -q and -s options
`smallif-all -q 70 -s 1920`
`smallif-all -q 70 -s 1920 --replace`

### Recursivity
For recursive, you can use :

`smallify-recurse`
(all sub-folders)

`smallify-recurse -d 2`
(2 sub-level depth)

for current folder only
`smallify-recurse -d 0`

* -d, --depth : choose level of recursivity

Other options ar the same.

* -h, --help    : display help
* -r, --replace : replace comiccs (BE CAREFUL !)
* -f, --folder  : choose a name for your smallified comics output folder
* -q QUALITY, --quality QUALITY : jpeg quality (0 to 100). default is 70
* -s SIZE, --size SIZE  Image height. default is 1920

`smallify-recurse -r` or `smallify-recurse --replace` will replace your comics, with a top-down recursivity.
Be careful !

Arguments can be mixed :

`smallify-recurse -d 0 -r`

`smallify-recurse -d0 -f "my folder"`

`smallify-recurse -q 70 -s 1920 -r`

## License
[GNU General Public License version 3](https://opensource.org/licenses/GPL-3.0)
