# RAG Data Poisoning Paper

IEEE conference-format paper for the RAG data-poisoning project.

## Files

- `main.tex` - IEEEtran manuscript
- `references.bib` - BibTeX references with verified arXiv metadata
- `figures/` - reserved for future figures generated from experiments

## Compile

Install a LaTeX distribution with `IEEEtran.cls`, then run:

```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

Or use `latexmk -pdf main.tex`.

The paper reports the current BAAI/bge-m3 experiment accurately: six synthetic
PDFs, ten categorized questions, top-k=3, mixed contamination of 40% (4/10),
and defended contamination of 0%. The original two-question pilot showed 100%
contamination. These are preliminary results, not a universal security
claim. The current untrusted document is a contamination proxy rather than a
fully optimized PoisonedRAG passage.

Source implementation:
https://github.com/takitahmid20/rag-data-poisoning
