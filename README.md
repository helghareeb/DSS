# DSS Book

LaTeX source for a Decision Support Systems (DSS) course book and its lecture
slides. The material is used to teach a DSS course and is organized as a
book-first repository: chapter sources live under `src/chapters`, and slide
decks live under `slides/src`.

## Repository Layout

- `src/main.tex`: main book entry point
- `src/chapters/`: numbered chapter files and supporting academic material
- `slides/src/`: Beamer slide sources, one file per chapter
- `slides/`: compiled slide PDFs
- `src/diagram.jpg`: figure used by the book

## Book Contents

The book currently covers 14 chapters:

1. Introduction to DSS
2. Decision Making Concepts
3. Decision Making Technologies and Environment
4. Model Management
5. Introduction to Machine Learning in DSS
6. Midterm Review and Sample Questions
7. Training of Classification Models
8. Supervised Learning for DSS
9. Automated Decision Systems and Expert Systems
10. Business Intelligence
11. Unsupervised Learning and Recommender Systems for DSS
12. Multi-Criteria Decision Analysis for DSS
13. Essay Questions with Model Answers
14. Acronyms and Definitions

## Build

### Compile the book

Run from the repository root:

```bash
(cd src && latexmk -pdf -interaction=nonstopmode main.tex)
```

This generates `src/main.pdf`.

### Compile all slides

Run from the repository root:

```bash
for f in slides/src/*.tex; do
  latexmk -pdf -interaction=nonstopmode -output-directory=slides "$f"
done
```

## Notes

- `slides/src/01.tex` is the chapter 01 slide deck; the remaining chapters have
  matching slide files in the same folder.
- Some root-level PDFs are intentionally ignored because they are local or
  legacy artifacts: `ai-.pdf`, `bio_.pdf`, `sw.pdf`, `لائحة الكلية.pdf`, and
  `DSS.pdf`.

## License

This repository is licensed under the
Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International
license. See [LICENSE](LICENSE).
