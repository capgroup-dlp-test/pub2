# pub2

Testing Git LFS setup.

## Setup

```sh
brew install git-lfs
git lfs install
git lfs track "*.bin" "*.png" "*.jpg" "*.zip" "*.pdf"
git add .gitattributes
```

Generate a test binary, then commit and push normally — LFS handles them automatically.

```sh
dd if=/dev/urandom of=test-binary.bin bs=1024 count=512
git add test-binary.bin
git commit -m "Add test binary"
git push
```

## Validate

```sh
git lfs ls-files
```

`*` = object present locally; `-` = pointer only (not downloaded).
