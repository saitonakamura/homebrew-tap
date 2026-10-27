# saitonakamura/homebrew-tap

Homebrew formulae for builds of my own forks.

## herdr

[saitonakamura/herdr](https://github.com/saitonakamura/herdr), a personal fork of
[herdrdev/herdr](https://github.com/herdrdev/herdr). It installs the fork's release
binaries for macOS and Linux (arm64 and x86_64), with `herdr-sidebar` beside `herdr`.

```sh
brew uninstall herdr            # if homebrew/core's herdr is installed: both own `herdr`
brew install saitonakamura/tap/herdr
```

Fork builds refuse `herdr update` and `herdr channel set`; upgrade with `brew upgrade`.

`Formula/herdr.rb` is generated. `.github/workflows/bump.yml` checks the fork for a
new release every hour and re-renders it with `scripts/render-formula <tag>
<SHA256SUMS>`; run the workflow by hand to pick a release up sooner.

herdr is Apache-2.0. The formula installs `LICENSE` and the release's notices
(`share/herdr/notices`) beside the binaries.
