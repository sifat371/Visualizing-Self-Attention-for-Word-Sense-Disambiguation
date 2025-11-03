# Visualizing-Self-Attention-for-Word-Sense-Disambiguation

This repository demonstrates a minimal self-attention model for simple word-sense disambiguation (WSD) on sentences containing the word "bank". The implementation is provided as interactive Jupyter notebooks that train a tiny PyTorch model and print attention weights so you can inspect which context words the model focuses on when deciding a sense.

Features
- Lightweight, educational example of self-attention for WSD.
- Implements a minimal single-layer self-attention model and visualizes attention weights.
- Small synthetic dataset with two classes: Financial and River.

Files
- [Visualizing-Self-Attention-for-Word-Sense-Disambiguation/SelfAtten.ipynb](Visualizing-Self-Attention-for-Word-Sense-Disambiguation/SelfAtten.ipynb) — main notebook with the model, training loop, and attention visualization.
- [SelfAtten.ipynb](SelfAtten.ipynb) — alternate copy of the notebook at the repository root.
- This README: [Visualizing-Self-Attention-for-Word-Sense-Disambiguation/README.md](Visualizing-Self-Attention-for-Word-Sense-Disambiguation/README.md)

Key symbols (open the notebook to inspect code)
- [`SimpleAttentionModel`](Visualizing-Self-Attention-for-Word-Sense-Disambiguation/SelfAtten.ipynb) — the model class that computes Q/K/V, attention weights, and final classification.
- [`sentence_to_tensor`](Visualizing-Self-Attention-for-Word-Sense-Disambiguation/SelfAtten.ipynb) — helper to convert sentences to token ID tensors.
- [`data`](Visualizing-Self-Attention-for-Word-Sense-Disambiguation/SelfAtten.ipynb) and [`vocab`](Visualizing-Self-Attention-for-Word-Sense-Disambiguation/SelfAtten.ipynb) — dataset and vocabulary defined in the notebook.

Requirements
- Python 3.8+
- Jupyter or JupyterLab / VS Code with Jupyter extension
- PyTorch (CPU or GPU build)

Install example (use a suitable command for your environment):
```sh
pip install torch jupyter
```

How to run
1. Open the notebook [Visualizing-Self-Attention-for-Word-Sense-Disambiguation/SelfAtten.ipynb](Visualizing-Self-Attention-for-Word-Sense-Disambiguation/SelfAtten.ipynb) in Jupyter or VS Code.
2. Install PyTorch if not present.
3. Execute the cells sequentially. The notebook:
   - builds the vocabulary,
   - defines [`SimpleAttentionModel`](Visualizing-Self-Attention-for-Word-Sense-Disambiguation/SelfAtten.ipynb),
   - trains the model,
   - prints predictions and attention weights for each sentence.

Notes
- This is an educational toy example intended to show attention behavior; it is not optimized for real WSD benchmarks.
- To extend: add batching, positional encodings, multiple attention heads, or a larger dataset.
