# Packaging

[![Please do not ship work in progress to users](https://dont-ship.it/dontshipwip.svg)](https://dont-ship.it/)

## Releases

### What is a release?

The [Semantic Versioning](https://semver.org/) is used for version numbering in this project.

A release is a [git tag](https://git-scm.com/docs/git-tag) in the `main` branch of the project's git repositry that starts with the letter `v` followed by the Semantic Versioning based version number.

### Creating a new release

1. Update the version number in the [`meson.build`](meson.build) file.
2. Write what happend from fixes, changes and updates and every thing in this release in the [CHANGELOG.md](CHANGELOG.md) file.
3. Add a new `<release>` tag under the `<releases>` tag in the [`data/io.github.zefr0x.hashes.metainfo.xml.in`](data/io.github.zefr0x.hashes.metainfo.xml.in) file with information about the release and a link to the CHANGELOG file.
4. Create a git commit with all of those changes.
5. Create a signed git tag with a `v` letter followed by the version number e.g. for `v1.5.3` you should do `git tag -s v1.5.3`.
6. Push changes to the remote using `git push origin main --tags`

## Official Packages

### Flatpak

To be added...

## What should be packaged?

Only stable [releases](#releases) should be packaged. Not an `alpha` nor a `beta` release should be.
