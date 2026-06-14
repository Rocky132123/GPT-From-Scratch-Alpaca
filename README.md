# GPT From Scratch on Alpaca Dataset

A GPT-style Large Language Model implemented from scratch in PyTorch and trained on the Alpaca instruction dataset.

## Project Overview

This project demonstrates the complete implementation of a decoder-only Transformer architecture without relying on Hugging Face model classes.

The model was trained on the Alpaca instruction dataset and is capable of generating coherent instruction-following responses.

## Features

- Decoder-only Transformer Architecture
- Multi-Head Causal Self-Attention
- Rotary Positional Embeddings (RoPE)
- RMSNorm
- SwiGLU Feed Forward Network
- SentencePiece BPE Tokenizer
- Custom Training Loop
- Top-k Sampling Text Generation
- Checkpoint Saving and Loading

---

## Model Architecture

```text
Input Tokens
      │
      ▼
Token Embedding
      │
      ▼
Transformer Blocks × N
      │
      ├── RMSNorm
      ├── Multi-Head Self Attention
      ├── RoPE
      ├── Residual Connection
      ├── RMSNorm
      ├── SwiGLU Feed Forward
      └── Residual Connection
      │
      ▼
Final RMSNorm
      │
      ▼
Linear Language Head
      │
      ▼
Next Token Prediction
