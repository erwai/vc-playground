# Mac M1 compatible Spleeter Docker Image

## Built the Docker Image

`docker build -t spleeter:aarch64 .`

Based on https://hub.docker.com/r/arm64v8/python/

Thanks to the discussions here: https://github.com/deezer/spleeter/issues/696, I've found out the packages/dependencies needed to be installed/built for aarch64.

## How to Use

`docker run --name spleeter_worker --rm -v $(pwd):/output spleeter:aarch64 spleeter separate -p spleeter:2stems -o output [file1] [file2]`

