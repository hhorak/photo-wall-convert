# Photo Wall Convert Tool
A simple tool to label and convert photographs for the big wall screen.

```
Usage: photo-wall-convert --event <event_title> [--quiet] [--crop] [--author <author>] <photo> [ <photo> ...]

Arguments:
  --event <event_title> is a short string
  --author <author> (optional) name of the person who took the photo that also holds the copyright; if omitted, it is taken from exif data
  --crop Crop the image to the expected ratio
  --open Open the output directory after conversion is done
  --quiet Do not write verbose output
```

