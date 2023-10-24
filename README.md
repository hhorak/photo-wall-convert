# Photo Wall Convert Tool
A simple tool to label and convert photographs for the big wall screen.

The tool serves primarily for adding an annotation with author and event name to the photo, and it also sets Copyright exif data.

The output is stored into the `./converted/` directory.

```
Usage: photo-wall-convert --event <event_title> [--quiet] [--crop] [--resize] [--author <author>] <photo> [ <photo> ...]

Arguments:
  --event <event_title> is a short string
  --author <author> (optional) name of the person who took the photo that also holds the copyright; if omitted, it is taken from exif data
  --crop Crop the image to the expected ratio
  --gravity <west|east> Whether the annotation should be on the left (west) or right (east), west is the default
  --resize Resize the photo to 7680x4820. If ommited, the text size will be adjusted in the same ratio as if the photo was 7680x4820.
  --open Open the output directory after conversion is done
  --quiet Do not write verbose output
```

## How to get the tool to your terminal

```
curl https://raw.githubusercontent.com/hhorak/photo-wall-convert/master/photo-wall-convert >/tmp/photo-wall-convert ; chmod a+x /tmp/photo-wall-convert
/tmp/photo-wall-convert -h
```

## Usage example

Suppose you are in the folder with photos `D123.JPG` and `D124.JPG`. Run the following command to convert the photos:

```
photo-wall-convert --event "DevConf.cz 2020" --author "Honza Horak" *.jpg *.JPG
```

This results in a new directory `./converted/` and the following two files annotated and converted to the expected size:
```
./converted/D123.JPG
./converted/D124.JPG
```

## License
This project is licensed under GNU General Public License v3.0.

## Credits
Thanks to Ondrej Ptak who sent me the original convert command.
