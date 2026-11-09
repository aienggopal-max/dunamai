# Dunamai

Dunamai is a Python library and CLI that generate version strings from version-control tags and commit history. It supports Git, Mercurial, Darcs, Subversion, Bazaar, Fossil, and Pijul. Output formats include PEP 440, Semantic Versioning, and custom templates.

This repository is owned by [aienggopal-max](https://github.com/aienggopal-max). It is a copy of [mtkennerly/dunamai](https://github.com/mtkennerly/dunamai), originally created by Matthew T. Kennerly. The imported commit attribution was rewritten for this copy. The upstream repository records the original authors and contributors.

## Install from source

Clone the repository with its full Git history. With a Python virtual environment active, install the checkout.

```sh
git clone https://github.com/aienggopal-max/dunamai.git
cd dunamai
python -m pip install .
```

## Quick start

Run these commands from a Git checkout with version tags. Dunamai uses tags such as `v1.26.5` to find the base version and counts commits since the tag. For an untagged commit, the default output also identifies the commit.

```sh
dunamai from git
dunamai from git --style semver --no-metadata
```

The library API exposes the same Git version.

```python
from dunamai import Version

print(Version.from_git().serialize())
```

## Documentation

- [Usage guide](docs/usage.md) for supported systems, tag patterns, archives, and build integration
- [CLI manual](docs/dunamai.1) and [API documentation source](docs/index.md)
- [Changelog](CHANGELOG.md)

## License

Dunamai is distributed under the [MIT License](LICENSE).
