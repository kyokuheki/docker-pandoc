# docker-pandoc
[![](https://images.microbadger.com/badges/version/kyokuheki/pandoc-typeset.svg)](https://microbadger.com/images/kyokuheki/pandoc-typeset "Get your own version badge on microbadger.com")
[![](https://images.microbadger.com/badges/image/kyokuheki/pandoc-typeset.svg)](https://microbadger.com/images/kyokuheki/pandoc-typeset "Get your own image badge on microbadger.com")

Containerized pandoc with Noto Sans CJKjp, Noto Serif CJKjp, Inconsolatazi4

## Usage
Convert markdown files

```sh
docker run -it --rm -v $PWD:/src kyokuheki/pandoc *.md
# or
docker run -it --rm -v $PWD:/src kyokuheki/pandoc *.md -o output.pdf
```

Execute pandoc

```sh
docker run -it --rm -v $PWD:/src --entrypoint pandoc kyokuheki/pandoc [arguments]...
```

enter console

```sh
docker run -it --rm -v $PWD:/src --entrypoint bash kyokuheki/pandoc
```

## Preset Configurations
- mainfont: TeX Gyre Termes (Ligatures=TeX,Scale=0.95)
- sansfont: TeX Gyre Heros (Ligatures=TeX,Scale=0.95)
- monofont: Inconsolatazi4
- luatexja-preset: noto-otf
- documentclass: ltjsarticle
- from: markdown_github+raw_tex
- pdf-engine: lualatex
