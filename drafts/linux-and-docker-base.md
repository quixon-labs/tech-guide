# Linux & Docker Notes

## Linux base

Ubuntu 18.04 LTS

### Rationale

[Linux Distributions Experience Report]()

## Docker bases

### Ordered by priority: 

- musl [pure statics]:
  - alpine
  - alpine derivatives

- glibc:
  - stretch
  - stretch derivatives
  - buildpack-deps:stretch
  - buildpack-deps:stretch derivatives
  - ubuntu:bionic
  - ubuntu:bionic derivatives

### Rationale

Not much additional rationale is needed, as almost all official docker images are based
on the stable debian base - it makes the most sense to utilise this to avoid redundant layers.
And of course, space constrained targets can utilise alpine which again has become the gold
standard for static binaries.