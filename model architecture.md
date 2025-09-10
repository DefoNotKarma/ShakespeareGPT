# Model Overview

- **Token Embedding:** `nn.Embedding(vocab_size, n_embd)` — maps tokens to embeddings.  
- **Position Embedding:** `nn.Embedding(block_size, n_embd)` — adds positional encoding.  
- **Transformer Blocks:**  
  - `blocks`: stack of `n_layer` transformer blocks (`Block(n_embd, n_head)`)  
  - **LayerNorm** applied after `blocks`  
  - `blocks2`: second stack of `n_layer` transformer blocks  
  - **LayerNorm** applied after `blocks2`  
- **Output Head:** `nn.Linear(n_embd, vocab_size)` — produces token logits.  

**Total Parameters:** ~0.409M

---

## Hyperparameters

| Parameter             | Value                        |
|-----------------------|------------------------------|
| Batch size            | 16                           |
| Context length        | 32                           |
| Embedding size        | 64                           |
| Attention heads       | 4                            |
| Number of layers      | 4 per block stack            |
| Dropout               | 0.0                          |
| Learning rate         | 0.001                        |
| Max iterations        | 5000                         |
| Evaluation interval   | 100 steps                    |
| Evaluation iterations | 200                          |
| Device                | GPU if available, else CPU   |
