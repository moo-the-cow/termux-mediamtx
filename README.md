# termux-mediamtx

This is an `nginx` build for Termux that includes `nginx-rtmp-module`.

## Pre-Requirements
```
pkg install termux-services
```

## Installation
```
mkdir $PREFIX/mediamtx && cd $PREFIX/mediamtx
curl -O https://github.com/moo-the-cow/termux-mediamtx/raw/main/mediamtx && \
curl -O https://github.com/moo-the-cow/termux-mediamtx/raw/main/mediamtx.yml
mkdir $PREFIX/var/service/mediamtx
echo "exec $PREFIX/mediamtx/mediamtx $PREFIX/mediamtx/mediamtx.yml" > $PREFIX/var/service/mediamtx/run
```

Hint: first time I had to restart the phone and then the following command worked
## Enable and Start Service
```sh
sv-enable mediamtx
sv up mediamtx
```
