
# Geographic Coverage and Retail Density Analysis of Bangladesh's National Distribution Network

CSE437 course project, Brac University (August 2026).

## Summary
Spatial analysis of about 832K retail shop records across Bangladesh's 8 divisions,
64 districts, and 515 upazilas. There is no supervised target. Four spatial methods
(grid counting, KDE, DBSCAN, Getis-Ord Gi*) are compared, with the Nearest-Neighbour
Index (NNI) as a global clustering test.

## Key results (as reported in the paper)
- Cleaned sample: 719,679 records
- 140 placeholder coordinate points (3,746 shops) detected and excluded from point-level analysis
- NNI = 0.0688 (strong clustering)
- Getis-Ord Gi* (999 permutations, k=5): 5 hotspots, 6 coldspots, 53 not significant
- Limitation: the Chittagong coldspot is sensitive to the spatial-weights choice

## Repository layout
- `notebooks/` : Phase 3 (cleaning, EDA, features) and Phase 4 (spatial methods)
- `outputs/` : result tables and figures
- `paper/` : IEEE-format report
- `data/` : download instructions only

## Data
Comprehensive Retail Network Dataset of Bangladesh, Mendeley Data,
DOI 10.17632/mgzvngzng2.1 (CC BY 4.0). See `data/README.md`.

## How to run

pip install -r requirements.txt

Download the dataset (see `data/README.md`), then run the notebooks in order.

## Authors
Wasib Ahmed Chayan, Nova Tasnim, Muhaimin Islam, Shajida Afrin Mim

## AI assistance disclosure
Claude (Anthropic) was used for brainstorming, literature search support, code
drafting, and checking statistics against the raw data. Analysis was run and
verified by the authors.

## License
Code: MIT. Dataset: CC BY 4.0 (original authors, see above).
EOF

cat > CITATION.cff << 'EOF'
cff-version: 1.2.0
message: "If you use this work, please cite it as below."
title: "Geographic Coverage and Retail Density Analysis of Bangladesh's National Distribution Network"
authors:
  - family-names: "Chayan"
    given-names: "Wasib Ahmed"
  - family-names: "Tasnim"
    given-names: "Nova"
  - family-names: "Islam"
    given-names: "Muhaimin"
  - family-names: "Mim"
    given-names: "Shajida Afrin"
date-released: 2026-08-01
license: MIT
