# Docker image to build FS-UAE
Docker debian image to build the amiga emulator [FS-UAE](https://fs-uae.net/).

## Create the image with the official repository
- `docker build -t fs-uae-build .`
## Create the image with another git repo
- `docker build -t fs-uae-build --build-arg FS_UAE_URL=https://github.com/prb28/fs-uae.git .`

## Run the image
- `docker run -it --name fs-uae fs-uae-build`

## Build FS-UAE steps
- `git pull`
- `./bootstrap`
- `./configure`
- `make`

## copy the resulting file from the container
- `docker cp fs-uae:/root/fs-uae/fs-uae ./fs-uae`