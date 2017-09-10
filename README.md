# Pandoc Book Maker Template
Template for creating epub books from markdown using `pandoc`.

[![forthebadge](http://forthebadge.com/images/badges/built-by-hipsters.svg)](http://forthebadge.com)

## Instructions

### Install Pandoc

#### Debian, Ubuntu, and derivatives
- With package: [pandoc-1.19.2.1-1-amd64.deb](https://github.com/jgm/pandoc/releases/download/1.19.2.1/pandoc-1.19.2.1-1-amd64.deb)

#### macOS
- With `brew`:
```bash
brew install pandoc
```
- With package: [pandoc-1.19.2.1-osx.pkg](https://github.com/jgm/pandoc/releases/download/1.19.2.1/pandoc-1.19.2.1-osx.pkg)

#### Windows
- With MSI: [pandoc-1.19.2.1-windows.msi](https://github.com/jgm/pandoc/releases/download/1.19.2.1/pandoc-1.19.2.1-windows.msi)

### Create Book
1. Change to this directory.
2. In `static/` directory, replace contents of `metadata.yml`, and `cover.jpg` with your own content.
3. In `chapters/` directory, add you content. Use file name to order the files as shown in the example.
4. Create your book with the following syntax below

#### EPUB

```bash
pandoc -S --epub-embed-font='fonts/*.ttf' -o target/book.epub static/metadata.yml chapters/*.md
```
Your book will be exported as`target/book.epub`.

#### PDF

```bash
pandoc -S -o target/book.pdf static/metadata.yml chapters/*.md
```
Your book will be exported as`target/book.pdf`.