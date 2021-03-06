
# Web Authentication Specification

This is the repository for the W3C WebAuthn Working Group, producing the draft **"Web Authentication"**

* [The editor's copy is available at https://w3c.github.io/webauthn/](https://w3c.github.io/webauthn/), or in the [`gh-pages` branch of this repository](https://github.com/w3c/webauthn/blob/gh-pages/index.html).
* [The build history is available at Travis-CI.org](https://travis-ci.org/w3c/webauthn/builds)
* [W3C WebAuthn Blog](https://www.w3.org/blog/webauthn/)
* [Web platform tests repository](https://github.com/w3c/web-platform-tests/tree/master/webauthn)

# Contributing

Before submitting feedback, please familiarize yourself with [our current issues list](https://github.com/w3c/webauthn/issues) and review the [mailing list discussion](https://lists.w3.org/Archives/Public/public-webauthn/).

# Building the Draft

Formatted HTML for the draft can be built using `bikeshed`:

```
$ bikeshed spec
```

You may also want to use the `watch` functionality to automatically regenerate as you make changes:

```
$ bikeshed watch
```

# Installation and Setup

You will need to have the Python tools `pygments` and `bikeshed` to build the draft. Pygments can be obtained via `pip`, but Bikeshed will need to be downloaded with `git`:

```
git clone --depth=1 --branch=master https://github.com/tabatkins/bikeshed.git ./bikeshed
pip install pygments
pip install --editable ./bikeshed
cp -R .spec-data/* ./bikeshed/bikeshed/spec-data
````

# Continuous Integration & Branches

This repository uses `.deploy-output.sh` to generate the Editor's Draft on the `gh-pages` branch upon every merge to `master`. In order to prevent failed merges during continuous integration, the formatted Editor's Draft should not be checked in to `master`, and it is in the `.gitignore` file.

