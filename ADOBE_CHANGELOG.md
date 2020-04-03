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

# Log

## v2.80-1.0.1-adobe

- fix async device startup

## v2.80-1.0.0-adobe

- SO_REUSEPORT
