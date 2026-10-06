# Low-Resource NLP From Scratch

A step-by-step path from machine learning fundamentals to low-resource NLP and LLM research. Every topic is implemented from scratch, then with standard tools, and the path leads to full paper reproductions.

**First milestone:** reproduce [MasakhaNER](https://arxiv.org/abs/2103.11811) (named entity recognition for African languages) by December 2026.

## Why this repo

I am a computer science master's student at Université de Lorraine (Nancy, France), preparing for research in low-resource NLP and large language models. This repo is my public lab notebook: one folder per topic, each with runnable code, a short write-up, and the results I actually obtained.

## Roadmap

### Phase 1: Foundations sprint

| # | Topic | Key concepts | Status |
|---|-------|--------------|--------|
| 01 | Decision trees | entropy, information gain, overfitting, train/test split | 🟡 |
| 02 | Linear and logistic regression | loss function, gradient descent, regularization | ⬜ |
| 03 | Neural networks from scratch | perceptron, backpropagation, activation functions | ⬜ |
| 04 | PyTorch fundamentals | tensors, autograd, training loop, optimizers | ⬜ |
| 05 | Text representation | tokenization, subwords (BPE), word embeddings | ⬜ |
| 06 | Sequence models | RNN, LSTM, sequence labelling, BIO tagging | ⬜ |
| 07 | Attention and the Transformer | self-attention, positional encoding, encoder | ⬜ |
| 08 | BERT | masked language modelling, pretraining, fine-tuning | ⬜ |
| 09 | NER in practice | Hugging Face `transformers`, `datasets`, span-level F1 (`seqeval`) | ⬜ |
| 10 | Multilingual models | mBERT, XLM-R, cross-lingual transfer | ⬜ |
| 11 | MasakhaNER reproduction, part 1 | data pipeline, baselines | ⬜ |
| 12 | MasakhaNER reproduction, part 2 | full experiments, comparison with the paper, write-up | ⬜ |

Status: ⬜ not started, 🟡 in progress, ✅ done

### Phase 2: Depth (2027 onwards)

Second paper reproduction, then: LLM internals, parameter-efficient fine-tuning (LoRA, adapters), data augmentation and transfer for low-resource languages, evaluation, machine translation, speech.

## Paper reproductions

| Paper | Task | My result | Paper result | Code |
|-------|------|-----------|--------------|------|
| MasakhaNER (Adelani et al., 2021) | NER, 10 African languages | *pending* | *pending* | [`reproductions/masakhaner`](reproductions/masakhaner) |

## Repository structure

```
.
├── phase1-foundations/
│   ├── 01-decision-trees/
│   │   ├── README.md          # what I learned, results, references
│   │   ├── decision_tree.py   # from-scratch implementation
│   │   └── experiments.ipynb  # experiments and plots
│   └── 02-.../
├── reproductions/
│   └── masakhaner/
├── notes/                     # glossary, paper summaries
├── requirements.txt
└── README.md
```

## How each topic is organised

1. **Concept**: explained in my own words in the topic's `README.md`, with the correct technical vocabulary.
2. **From scratch**: implemented with NumPy or plain PyTorch, no shortcuts.
3. **With the standard library**: the same thing with scikit-learn, PyTorch or Hugging Face, and a comparison of the results.
4. **Experiments**: what happens when I change hyperparameters, data size, or the model.

## Running the code

```bash
git clone https://github.com/mbianytabs/low-resource-nlp-from-scratch.git
cd low-resource-nlp-from-scratch
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python phase1-foundations/01-decision-trees/decision_tree.py
```

## Contact

TABE-OJONG Manuel, M1 Computer Science, Université de Lorraine
manuel.tabe-ojong2@etu.univ-lorraine.fr || tabeojong23@gmail.com

This project is licensed under the [MIT License](LICENSE).
