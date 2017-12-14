# rpi-shairport

A Docker image to run [shairport-sync](https://github.com/mikebrady/shairport-sync) on a Raspberry Pi.

Tested on a Raspberry Pi 3 running Debian Jessie.

[Dockerhub](https://hub.docker.com/r/svanscho/rpi-shairport/): [![](https://images.microbadger.com/badges/version/svanscho/rpi-shairport.svg)](https://microbadger.com/images/svanscho/rpi-shairport "Get your own version badge on microbadger.com") [![](https://images.microbadger.com/badges/image/svanscho/rpi-shairport.svg)](https://microbadger.com/images/svanscho/rpi-shairport "Get your own image badge on microbadger.com") 

# Usage

## From Dockerhub (Recommended)

```sh
$ docker run -d --restart always \
                --name rpi-shairport \
                --net host \
                --device /dev/snd \
                svanscho/rpi-shairport
```

## Building from scratch

```sh
$ git clone https://github.com/svanscho/rpi-shairport/
$ cd rpi-shairport
$ docker build . -t rpi-shairport
$ docker run -d --restart always \
                --name rpi-shairport \
                --net host \
                --device /dev/snd \
                rpi-shairport
```

---

The server will now show up on your macOS and iOS devices and you should be able to play music to them.
