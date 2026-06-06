# TIF360 - Context-Aware Sarcasm Detection in Social Media

This repository contains the submission notebooks for the TIF360 project on sarcasm detection across Twitch and Reddit.

## Repository layout

- `Notebooks/jupyter-notebook/`: final notebooks
- `Dataset/`: local data layout expected by the notebooks
- `Notebooks/jupyter-notebook/checkpoints/`: optional saved DistilBERT checkpoints created during notebook execution
- `Notebooks/figures/`: generated figures exported by the analysis notebooks

## Environment

Install the notebook dependencies with:

```bash
python3 -m pip install -r requirements.txt
```

## Dataset layout

The raw datasets are not committed to this repository.

Expected local paths:

- `Dataset/Twitch/train.csv` and `Dataset/Twitch/test.csv`
- or `Dataset/Twitch.zip`
- `Dataset/Reddit/train-balanced-sarcasm.csv`
- or `Dataset/Reddit/train-balanced-sarc.csv.gz`
- or `Dataset/Reddit/train-balanced-sarc.csv/train-balanced-sarc.csv`

Optional Reddit files:

- `Dataset/Reddit/test-balanced.csv`
- `Dataset/Reddit/test-unbalanced.csv`

Additional details are listed in [Dataset/README.md](Dataset/README.md).

## Dataset sources

The project topic sheet lists the following public sarcasm-dataset sources:

- [Kaggle: Sarcasm Dataset](https://www.kaggle.com/datasets/danofer/sarcasm)
- [Kaggle: Tweets With Sarcasm And Irony](https://www.kaggle.com/datasets/nikhiljohnk/tweets-with-sarcasm-and-irony)

## Suggested execution order

1. `Notebooks/jupyter-notebook/sarcasm-detection-comparison.ipynb`
2. `Notebooks/jupyter-notebook/sarcasm-detection-cleaned-twitch-ablations.ipynb`
3. `Notebooks/jupyter-notebook/reddit-sarcasm-comment-vs-context-colab.ipynb`
4. `Notebooks/jupyter-notebook/reddit-sarcasm-distilbert-comment-vs-context-colab.ipynb`
5. `Notebooks/jupyter-notebook/reddit-sarcasm-linguistic-cues-and-distilbert-errors.ipynb`

The final Reddit analysis notebook can still run without saved DistilBERT checkpoints, but its qualitative error analysis is richer if notebook 4 has already been executed.
