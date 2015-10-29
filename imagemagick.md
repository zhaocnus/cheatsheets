#ImageMagick commands

* batch convert transprant png to jpg
```bash
mogrify -resize 16x12 -quality 100 -format jpg -background white -path ./output ./input/*.png
```
