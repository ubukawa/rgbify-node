# rio-rgbify-node
unvt/rgbify revised to add nodejs

# background
I wanted to use both nodejs and raterio to convert SRTM data into RGB elevation tiles.

# use
```zsh
docker run -ti --rm -v ${pwd}:/root/work unvt/rgbify-node
```

# build
```zsh
rake build
```