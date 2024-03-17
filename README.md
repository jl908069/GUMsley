# GUMsley

Data and code for EACL 2024 paper [GUMsley: Evaluating Entity Salience in Summarization for 12 English Genres](https://aclanthology.org/2024.eacl-long.158/&target=_blank)

## Directories
- All 213 gold (GUMv9) summaries and their corresponding machine-generated summaries are in the `data` folder
  - The letter `b` and `c` in the file names represent BRIO style (one-sentence) and CTRLSum style (2-3 sentences) summary, respectively. See the paper for how we control the length of the summary

- Machine-generated summaries and the full text for GUMv9 test set (24 documents) are in the `GUM9_test` folder

## Files
- `Eval.ipynb`: summary level evaluation using **ROUGE scores** (Lin, 2004) and **BERTScore** (Zhang et al., 2020) (on the entire dataset)
- `SummaC.ipynb`: evaluation on entity hallucination using **SummaC<sub>Conv</sub> scores** (Laban et al., 2022) (on test set)


## Entity salience data
Go to the <a href="https://github.com/amir-zeldes/gum/tree/master" target="_blank">GUM repo</a> for entity salience data

coref/ - Entity and coreference annotation in two formats:
  - conll/ - CoNLL shared task tabular format (with Wikification but no bridging or split antecedent annotations)
  - tsv/ - WebAnno .tsv format, including entity type, salience and information status annotations, Wikification, bridging, split antecedent and singleton entities
