# TikzGraphs

This library generates graph layouts using the TikZ graph layout package.


You must also have the LaTeX package PGF/TikZ version 3.0 or later installed. You may download this from [http://www.ctan.org/pkg/pgf CTAN], either directly or through your LaTeX package manager. If you are using the texlive package manager, this may be done by running `tlmgr install pgf` from the command line.

## Example

```julia
using Graphs
using TikzGraphs
g = simple_graph(4)
add_edge!(g, 1, 2)
add_edge!(g, 2, 3)
add_edge!(g, 3, 4)
add_edge!(g, 1, 4)
plot(g)
```

## Saving plots

```julia
using Graphs
using TikzGraphs
using TikzPictures
g = simple_graph(4)
add_edge!(g, 1, 2)
add_edge!(g, 2, 3)
add_edge!(g, 3, 4)
add_edge!(g, 1, 4)
t = plot(g)
save(PDF("graph"), t)
save(SVG("graph"), t)
```
