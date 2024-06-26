# Release Checklist

The following is the release checklist for each version of `river`.

* [ ] Open a PR changing the version of `river` in `Cargo.toml`, and adding a
      document to the `docs/release-notes` containing the major changes in
      this release.
* [ ] Merge the PR
* [ ] Locally, pull the up to date `main` branch
* [ ] Tag the commit with `git tag vX.Y.Z`
* [ ] Push the tag to github with `git push origin --tags`
* [ ] Wait for the `cargo-dist` job to complete.
    * This will create the release on github
* [ ] Release to crates.io using `cargo publish`
* [ ] Edit the release on github, using the "Generate release notes" feature.
      Move the generated "What's Changed" section to the top of the release.
* [ ] If we made any changes to the configuration file format or other major changes,
      make a PR to the [Homebrew formula] (only necessary for breaking changes, otherwise
      it should "autobump" when the new GH release is noticed).
* [ ] Announce the release in various places

[Homebrew formula]: https://github.com/Homebrew/homebrew-core/blob/master/Formula/r/river.rb
