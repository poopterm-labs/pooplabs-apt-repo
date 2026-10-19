# Poop Labs APT Repository

A package feed for jailbreak software maintained by [poopterm-labs](https://github.com/poopterm-labs).

## Add to Cydia

Add this source in Cydia under **Sources → Edit → Add**:

`https://poopterm-labs.github.io/pooplabs-apt-repo/`

This feed is for `iphoneos-arm` packages.

## Publish a package

Upload a `.deb` file into `debs/` on the `main` branch. GitHub Actions will generate `Packages`, `Packages.gz`, and `Release`, then publish the feed to GitHub Pages.

Before the first deploy, open **Settings → Pages** and set the build and deployment source to **GitHub Actions**. The feed URL will become available after the Pages deployment succeeds.
