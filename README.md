# pub2

Testing Git LFS setup.

## Setup

```sh
brew install git-lfs
git lfs install
git lfs track "*.bin" "*.png" "*.jpg" "*.zip" "*.pdf"
git add .gitattributes
```

Then commit and push binary files normally — LFS handles them automatically.

## Validate

```sh
git lfs ls-files
```

`*` = object present locally; `-` = pointer only (not downloaded).
