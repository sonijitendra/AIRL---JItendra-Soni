# AIRL Internship - Submission Repo

This repository contains the required notebooks for the AIRL internship assignment.

## Files
- `q1.ipynb` — Vision Transformer (ViT) trained on CIFAR-10 (PyTorch). Implements patch embedding, positional embeddings, CLS token, transformer encoder blocks, and training/eval code. Run on Google Colab (GPU).
- `q2.ipynb` — Text-driven segmentation pipeline using SAM and a grounding model (high-level runnable Colab notebook with install cells and example flow). Replace placeholders with SAM checkpoint paths to run end-to-end.
- `README.md` — This file.

## How to run (Colab)
1. Open each notebook in Google Colab.
2. Runtime > Change runtime type > GPU.
3. Run cells top-to-bottom. For Q2, you will need to download SAM/GroundingDINO checkpoints as instructed in the notebook.

## Q1 — Best config (example)
- `img_size=32`, `patch_size=4`, `emb_dim=192`, `depth=6`, `num_heads=3`, `batch_size=128`, `epochs=20`
- Reported test accuracy (example): **depends on training**. Try increasing epochs, model size or using pretrained ViT from `timm` for higher performance.

## Notes & Tips
- Keep the repo limited to exactly the 3 files before submission (q1.ipynb, q2.ipynb, README.md).
- Include any concise analysis (patch choices, augmentations, optimizer/scheduler) inside README or a short section in the notebook for bonus marks.
- If you want, I can help further by improving the ViT (add mixup, weight decay tuning, pretrained fine-tuning), or adapt Q2 to a specific public SAM checkpoint.
