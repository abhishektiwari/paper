# Paper Template
Template repository to write academic research paper using markdown and generate PDF using Pandoc.

1. Create a new Github repository using this template.

2. After creating repository, enable `Workflow permissions` to `Read and write permissions` for your Github repository by going to `Settings` → `Actions` → `General`. 

## Steps for local build

- Update paper metadata `metadata.yaml`
- Update paper content `article.md`
- Update the citation `article.bibtex`
- Add images to `images` folder and refrence in `article.md`
- Run the build `bash build.sh` to generate `article.pdf`

## Steps for Action build

- Commit your paper changes and push.
- If you have changed the following folders Github Action will perform `article.pdf` build. Due to large size of `texlive-full`, currently build takes anywhere between 6-8 minutes.
    - `paper/**`
    - `paper/images/**`
    - `csl/**`
    - `data/templates/**`
- On successful build `article.pdf` will be uploaded to `Releases` section of your Github repository. 


# Prerequisite
On Mac Install `texlive`, `pandoc` using `brew`,

```
brew install pandoc texlive
```

Install only required `texlive` packages,
```
sudo tlmgr install beamerarticle pgfpages amsmath amssymb setspace inputenc mathspec unicode-math lmodern xeCJK upquote parskip fancyvrb xcolor hang flushmargin bottom multiple adjustbox graphicx listings etoolbox fvextra multirow longtable booktabs array caption headsepline footsepline titling footnotebackref sourcesanspro mdframed csquotes pagecolor afterpage tikz hyperref bookmark biblatex selnolig natbib babel calc subcaption soul luacolor svg float ccicons
```

Alternatively, install `texlive-full`,

```
brew install pandoc texlive-full
```