
# GPT-Style Transformer from Scratch

A PyTorch project exploring language modeling, from a simple Bigram model to a GPT-style Transformer.

The goal is to understand Transformer architectures, implement their main components, and progressively develop a small conversational language model.

### Model Architecture

Implemented a decoder-only Transformer featuring:
- 6 Transformer blocks and 6 attention heads
- 384-dimensional embeddings
- Causal self-attention, feed-forward networks and residual connections
- Character-level tokenization with a 256-token context window

### Experiments and Results

#### Experiment 1: Tiny Shakespeare

Implemented a Bigram baseline and a Transformer to compare their language modeling performance.

| Model | Best validation loss |
|---|---:|
| Bigram | ~2.48 |
| Transformer | ~1.49 |

#### Experiment 2: SimpleStories

Trained the Transformer from scratch on a larger dataset to improve text generation and generalization.

- 93,000 training stories and 7,000 validation stories
- 8,000 training iterations
- Final validation loss: approximately 0.75
- No significant overfitting observed

The model generates more natural English sentences but still struggles with spelling and narrative coherence.

### Limitations and Next Steps

Current limitations include character-level tokenization, a short context window and difficulties maintaining logical consistency.

Planned improvements:
- Subword tokenization (BPE)
- Longer context windows
- Instruction fine-tuning for question answering

### Running the Project

The notebooks can be opened and executed in Google Colab. Training datasets are loaded from their original sources.

### References & Acknowledgements

This project was developed as a learning exercise, drawing on existing implementations and technical documentation.

- [Andrej Karpathy — Let's build GPT from scratch](https://github.com/karpathy/ng-video-lecture)
- [Attention Is All You Need — Vaswani et al.](https://arxiv.org/abs/1706.03762)
- [SimpleStories Dataset](https://huggingface.co/datasets/SimpleStories/SimpleStories)
- [PyTorch Documentation](https://docs.pytorch.org/docs/stable/index.html)
