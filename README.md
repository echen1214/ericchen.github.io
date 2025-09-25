# About Me
<!-- 
[<img alt="Static Badge" src="https://img.shields.io/badge/%F0%9F%AA%B4%20Houseplant%20-x?style=flat&amp;label=Project%20type&amp;color=1E1E1D">](https://www.hannahilea.com/blog/houseplant-programming) -->

My personal website and the lightweight pandoc-based Julia script that builds it. Site can be viewed at [eric_anth_chen.com](https://www.eric_anth_chen.com).

Super grateful for [Hannah Robertson](https://hannahilea.com/), whom I connected with during the Recurse Center for pointing me towards the right directions and allowing me to fork her personal website.

## Usage

### Use template to add new content

Run `julia --startup-file=no add_stuff.jl <ARG>` with arg `blog` or `p5`.

### Site generation

Static site generation is managed by Julia script [`build-site/run.jl`](./build-site/run.jl). This process (1) converts markdown src.md (blog) files to html, (2) regenerates both the project and blog index.html pages, and (3) regenerates the RSS feed. Generated html can then be committed along with the changed source. 

When working in VSCode IDE with the [Run on Save](https://marketplace.visualstudio.com/items?itemName=emeraldwalk.RunOnSave) plugin installed, this generation runs automatically whenever an edited document is saved.

To run manually it, do `julia build-site/run.jl`.

Build dependencies:
- Requires a local installation of Julia
- Requires a local installation of [prettier](https://formulae.brew.sh/formula/prettier)
