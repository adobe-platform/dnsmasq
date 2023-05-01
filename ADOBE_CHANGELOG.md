# About

We maintain a set of patches on top of upstream dnsmasq. They need to be
semantically versioned as well so we understand, for example, that we're
upgrading a fix version of dnsmasq vs. a fix version of our patches.

The scheme is quite simple. The upstream version is first, followed by a hyphen,
followed by our version:

```
D stand for dnsmasq
A stands for Adobe's changes

v{D major}.{D minor/fix}-{A major}.{A minor}.{A fix}-adobe
```
# Build
```commandline
Use the below comands to build and push multi-arch images using buildx.

1. Create a new builder instance

$ docker buildx create --name <builder_instance_name>

2. Use the created builder instance

$ docker buildx use <builder_instance_name>

3. Build and push multi-arch image

$ docker buildx build --platform linux/amd64,linux/arm64 --tag <docker_repo>/net/dnsmasq:<version> --push .
```

# Log

## v2.90-1.4.0-adobe

- built from v2.90 (9bbf098a970c9e5fa251939208e25fb21064d1be)


## v2.89-1.4.0-adobe

- built from v2.89
- upgraded to ubuntu:22.04

## v2.85-1.3.0-adobe

- Enabling multi-arch builds

## v2.85-1.2.0-adobe

- built from v2.85
- upgraded to ubuntu:20.04

## v2.80-1.0.1-adobe

- fix async device startup

## v2.80-1.0.0-adobe

- SO_REUSEPORT
