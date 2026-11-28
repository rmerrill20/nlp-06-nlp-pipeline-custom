# Web Mining and Applied NLP Project Report

Web Mining and Applied NLP | Project 06

Author: Ronni Merrill

Date: 2026 November

## Overview

This project introduces a complete
natural language processing pipeline
for analyzing text extracted a healthcare-
realted research article titled
Protecting Patient Privacy in Clinical
Foundation Models: Technical and Legal
Perspectives.

The objective is to acquire HTML,
validate document structure,
extract and clean text,
engineer NLP features,
analyze vocabulary patterns,
and persist the results.

The project extends the earlier EVTL architecture
by introducing an explicit Analyze stage.

The resulting architecture is
Extract, Validate, Transform, Analyze, Load (EVTAL).

The purpose of this analysis is to process the
article's text and identify frequently occurring
words that help describe its content.

As a technical modification, the original data source
was replaced with the selected arXiv research article:

https://arxiv.org/abs/2608.07705

This change adapts the existing NLP pipeline to a
healthcare topic involving a patient privacy and
clinical artificial intelligence.

## Tools and Methods

The project uses:

- Python for pipeline orchestration and processing.
- Requests for retrieving HTML documents.
- BeautifulSoup for parsing and extracting HTML content.
- spaCy for tokenization and linguistic text processing.
- Pandas for structured data transformation.
- Token counts and type-token ratios for describing vocabulary.
- Matplotlib for token frequency visualizations.
- WordCloud for visual exploration of vocabulary.
- CSV for persistent output.
- Logging for execution records.
- Ruff, ty, and pytest for code verification.
- Zensical and GitHub Pages for published documentation.

This customized project uses an arXiv article that is different
from the example project.

The pipeline implements five stages:

- **Extract** - retrieve HTML and preserve the raw document.
- **Validate** - verify the expected HTML structure.
- **Transform** - extract metadata, clean text, and engineer NLP features.
- **Analyze** - compute token frequencies and create visualizations.
- **Load** - save the processed dataset to a CSV file.

The Transform stage uses spaCy
with the `en_core_web_sm` English language model.

The example calculates token counts,
unique token counts, type-token ratios,
and other derived text features.

The Analyze stage produces a token frequency chart
and a word cloud.

Technical Modification: 15 tokens

This project modifies the token-frequency analysis
to display the top 15 most common tokens.

This adjustment provides a more concise view of the
most frequently occurring vocabulary while preserving
the existing text-processing and analysis workflow.

## Verification

A successful execution displays:

    Pipeline executed successfully!

The pipeline records execution details in a project log.

The following artifacts are created:

- `data/raw/case_raw.html` - original HTML document.
- `data/processed/case_processed.csv` - processed NLP dataset.
- `data/processed/case_top_tokens.png` - token frequency chart.
- `data/processed/case_wordcloud.png` - word cloud visualization.

These results demonstrate that the pipeline can
acquire, validate, transform, analyze,
and persist web text data.

Automated tests provide additional verification
of the pipeline's expected behavior.

## Interpretation

Natural language processing requires
more than extracting text from documents.

Text must be represented in ways
that support meaningful analysis.

Token frequencies describe recurring vocabulary,
while unique token counts and type-token ratios
provide measures of vocabulary diversity.

The top 15 token analysis provides a focused
view of the most frequently occurring words in
the selected research article. These terms can
help identify recurring concepts related to
patient privacy, clinical artificial
intelligence, and data protection.

Visualizations help reveal dominant terms
and suggest questions for further investigation.

Preprocessing decisions affect these results.
Removing punctuation, normalizing text,
and filtering stopwords may reduce noise,
but can also remove meaningful linguistic information.

These techniques remain relevant
for inspectable NLP workflows,
even as modern language models provide
additional approaches to language understanding.

## Documentation Index

- **Home** - this landing page
- [**Project Instructions**](project-instructions.md)
- [**Glossary**](glossary.md)
- [**NLP Evolution**](nlp-evolution.md)

## Project Links

- [GitHub Repository](https://github.com/denisecase/nlp-06-nlp-pipeline)
- [Example Pipeline](https://github.com/denisecase/nlp-06-nlp-pipeline/blob/main/src/nlp/pipeline_web_html.py)
- [Example Configuration](https://github.com/denisecase/nlp-06-nlp-pipeline/blob/main/src/nlp/config.py)
- [Transform Stage](https://github.com/denisecase/nlp-06-nlp-pipeline/blob/main/src/nlp/stage03_transform.py)
- [Analyze Stage](https://github.com/denisecase/nlp-06-nlp-pipeline/blob/main/src/nlp/stage04_analyze.py)

## Project Resources

- [Project Instructions](project-instructions.md)
- [NLP Evolution](nlp-evolution.md)
- [Professional Python Guide](https://denisecase.github.io/pro-analytics-02/)
- [Professional Python Project Explainer](https://pup-pack.github.io/professional-python-project-explainer/)
