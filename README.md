# Build-Essential Official Image Build

## Description

A Docker for trusted software builds.
Provides a trusted and easy way to build applications and their containers.

The official Docker images are hosted on [Continuul's Docker Hub for Build-Essential](https://hub.docker.com/r/continuul/build-essential/).

There are several pieces that are used to build this image:

* We start with an Alpine base image, and add the Go language tools, and the alpine-sdk,
  an equivalent to Ubuntu build-essentials.
* We add openssh, zip and bash.

## Usage

For example,

```bash
: ${HERMETIC_BUILD_DIR:=/go/src/${SELF_ROOT#*$GOPATH/src/}}
 docker run --rm -e "BUILD_TAGS=$BUILD_TAGS" -v "$(pwd)":${HERMETIC_BUILD_DIR} -w ${HERMETIC_BUILD_DIR} \
    continuul/build-essential ./scripts/dist_build.sh
```

## Contents

The Docker contains the following installed software for building software:

- fakeroot (1.21-r1)
- sudo (1.8.19_p1-r0)
- libcap (2.25-r1)
- pax-utils (1.1.6-r0)
- libressl (2.4.4-r0)
- libattr (2.4.47-r4)
- attr (2.4.47-r4)
- tar (1.29-r1)
- pkgconf (1.0.2-r0)
- patch (2.7.5-r1)
- libssh2 (1.7.0-r2)
- libcurl (7.52.1-r2)
- curl (7.52.1-r2)
- abuild (2.29.0-r2)
- binutils-libs (2.27-r0)
- binutils (2.27-r0)
- gmp (6.1.1-r0)
- isl (0.17.1-r0)
- libgomp (6.2.1-r1)
- libatomic (6.2.1-r1)
- libgcc (6.2.1-r1)
- mpfr3 (3.1.5-r0)
- mpc1 (1.0.3-r0)
- libstdc++ (6.2.1-r1)
- gcc (6.2.1-r1)
- make (4.2.1-r0)
- musl-dev (1.1.15-r6)
- libc-dev (0.7-r1)
- fortify-headers (0.8-r0)
- g++ (6.2.1-r1)
- build-base (0.4-r1)
- expat (2.2.0-r0)
- pcre (8.39-r0)
- git (2.11.1-r0)
- xz-libs (5.2.2-r1)
- lzo (2.09-r1)
- squashfs-tools (4.3-r3)
- libburn (1.4.6-r0)
- ncurses-terminfo-base (6.0-r7)
- ncurses-terminfo (6.0-r7)
- ncurses-libs (6.0-r7)
- libedit (20150325.3.1-r3)
- libacl (2.2.52-r2)
- libisofs (1.4.6-r0)
- libisoburn (1.4.6-r0)
- xorriso (1.4.6-r0)
- acct (6.6.2-r0)
- lddtree (1.25-r2)
- libuuid (2.28.2-r1)
- libblkid (2.28.2-r1)
- device-mapper-libs (2.02.168-r3)
- cryptsetup-libs (1.7.2-r1)
- kmod (23-r1)
- mkinitfs (3.0.9-r1)
- mtools (4.0.18-r1)
- alpine-sdk (0.5-r0)
- readline (6.3.008-r4)
- bash (4.3.46-r5)
- openssh-client (7.4_p1-r0)
- openssh-sftp-server (7.4_p1-r0)
- openssh (7.4_p1-r0)
- libffi (3.2.1-r2)
- gdbm (1.12-r0)
- yaml (0.1.7-r0)
- ruby-libs (2.3.3-r0)
- ruby (2.3.3-r0)
- ruby-io-console (2.3.3-r0)
- ruby-bundler (1.13.4-r0)
- zip (3.0-r4)
