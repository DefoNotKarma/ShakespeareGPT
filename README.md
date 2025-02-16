model currently unrefined. 

current architecture:
======================================================================
Layer (type:depth-idx)                        Trainable
======================================================================
BigramLanguageModel                           True
├─Embedding: 1-1                              True
├─Embedding: 1-2                              True
├─Sequential: 1-3                             True
│    └─Transformer_block: 2-1                 True
│    │    └─LayerNorm: 3-1                    --
│    │    └─Multi_Head_Attention: 3-2         True
│    │    └─LayerNorm: 3-3                    --
│    │    └─Feed_Forward: 3-4                 True
│    └─Transformer_block: 2-2                 True
│    │    └─LayerNorm: 3-5                    --
│    │    └─Multi_Head_Attention: 3-6         True
│    │    └─LayerNorm: 3-7                    --
│    │    └─Feed_Forward: 3-8                 True
│    └─Dropout: 2-3                           --
│    └─Transformer_block: 2-4                 True
│    │    └─LayerNorm: 3-9                    --
│    │    └─Multi_Head_Attention: 3-10        True
│    │    └─LayerNorm: 3-11                   --
│    │    └─Feed_Forward: 3-12                True
│    └─Dropout: 2-5                           --
│    └─Transformer_block: 2-6                 True
│    │    └─LayerNorm: 3-13                   --
│    │    └─Multi_Head_Attention: 3-14        True
│    │    └─LayerNorm: 3-15                   --
│    │    └─Feed_Forward: 3-16                True
│    └─LayerNorm: 2-7                         --
│    └─Dropout: 2-8                           --
├─Linear: 1-4                                 True
======================================================================
Total params: 197,436
Trainable params: 197,436
Non-trainable params: 0
Total mult-adds (Units.MEGABYTES): 1.99
======================================================================
Input size (MB): 0.01
Forward/backward pass size (MB): 11.19
Params size (MB): 0.79
Estimated Total Size (MB): 11.98
======================================================================
