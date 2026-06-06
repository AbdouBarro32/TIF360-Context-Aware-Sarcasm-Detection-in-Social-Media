# Dataset Layout

The repository does not track the raw dataset files. Place the local data under the following paths before running the notebooks.

## Topic C sources

The course topic sheet points to these public dataset sources:

- [Kaggle: Sarcasm Dataset](https://www.kaggle.com/datasets/danofer/sarcasm)
- [Kaggle: Tweets With Sarcasm And Irony](https://www.kaggle.com/datasets/nikhiljohnk/tweets-with-sarcasm-and-irony)

## Twitch

Supported options:

- `Dataset/Twitch/train.csv` and `Dataset/Twitch/test.csv`
- `Dataset/Twitch.zip`

The Twitch notebooks will read directly from the extracted CSV files when available, and otherwise fall back to `Dataset/Twitch.zip`.

## Reddit

Supported training-file options:

- `Dataset/Reddit/train-balanced-sarcasm.csv`
- `Dataset/Reddit/train-balanced-sarc.csv.gz`
- `Dataset/Reddit/train-balanced-sarc.csv/train-balanced-sarc.csv`

Optional auxiliary files:

- `Dataset/Reddit/test-balanced.csv`
- `Dataset/Reddit/test-unbalanced.csv`

The Reddit notebooks search for the supported training-file names automatically, so the large training CSV does not need to be stored under more than one format.
