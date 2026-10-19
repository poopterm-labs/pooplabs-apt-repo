# Poop Labs APT Repository

A flat APT package feed for Debian packages and jailbreak packages maintained by [poopterm-labs](https://github.com/poopterm-labs).

## Add to Cydia

Add this source in Cydia under **Sources → Edit → Add**:

`https://poopterm-labs.github.io/pooplabs-apt-repo/`

The iOS packages in this feed use the `iphoneos-arm` architecture.

## Add to Debian

Add this line to an APT source file (for example, `/etc/apt/sources.list.d/pooplabs.list`):

```text
deb [trusted=yes] https://poopterm-labs.github.io/pooplabs-apt-repo/ ./
```

This is an unsigned personal repository. `trusted=yes` tells APT to accept its packages without signature verification; use it only if you trust the repository and its maintainers. APT will choose packages compatible with the Debian machine's architecture.

## Publish a package

Put each `.deb` directly in `debs/` on the `main` branch. The package's `Architecture` field is included in the generated feed, so the same repository can contain Debian packages for multiple architectures alongside `iphoneos-arm` jailbreak packages. GitHub Actions generates `Packages`, `Packages.gz`, and `Release`, then publishes them to GitHub Pages.

The latest stable Poopterm `amd64` package is imported from its GitHub release automatically during the hourly feed refresh.

Before the first deployment, open **Settings → Pages** and set the build and deployment source to **GitHub Actions**.
