# treevis

Stacked, time-aligned views of genealogies from the backsel MCMC.

**Viewer:** https://mashanaslidnyk.github.io/treevis/

## Adding trees

Put Auspice v2 JSONs in `auspice/`, then commit and push. They show up in the viewer about a minute later.

Files called `treevis_<dataset>_<panel>.json` are grouped into one dataset, with one panel per file. For example, `treevis_burst_N1250_1Ne_true.json`, `..._inferred_backsel.json` and `..._inferred_neutral.json` make up the dataset `burst/N1250/1Ne` with three panels. Panel names must be `true` or start with `inferred_`, and `true` always goes on top. The grouping rule lives at the top of the script in `index.html` (`GROUP` and `ORDER`).

Link to a dataset with a hash, e.g. `https://mashanaslidnyk.github.io/treevis/#cont/N2500/2Ne`.

The same files still work on Nextstrain: https://nextstrain.org/community/MashaNaslidnyk/treevis

## Local preview

    python3 -m http.server 8000    # from the repo root, then open http://localhost:8000
