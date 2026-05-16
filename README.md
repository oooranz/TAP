# 🚰 TAP

[![arXiv](https://img.shields.io/badge/arXiv-2605.10315-b31b1b.svg)](https://arxiv.org/abs/2605.10315)

Initial code release for the paper [ICML 2026] [Active Tabular Augmentation via Policy-Guided Diffusion Inpainting](https://arxiv.org/abs/2605.10315).

High-fidelity tabular generators don't necessarily help downstream learners, a phenomenon we call the *fidelity-utility gap*. **TAP** closes it by bringing RLVR-style policy learning to tabular augmentation. We pair a frozen diffusion inpainter with a lightweight policy that learns *what* to generate and *when* to inject, using a tabular foundation model (TabPFN) as a fast online utility estimator. Augmentation becomes an active, sequential decision process rather than passive sampling, with explicit gating and conservative windowed commitment ensuring safe injection under data scarcity.

## Setup

```bash
pip install -r requirements.txt
```

## **Quickstart**

Classification on your own data:

```bash
python run_tap.py \
  --dataset my_classification_run \
  --data_path path/to/your_data.csv \
  --target_col label \
  --task_type classification \
  --n_real 50 \
  --final_samples 500 \
  --device cuda
```

Regression on your own data:

```bash
python run_tap.py \
  --dataset my_regression_run \
  --data_path path/to/your_data.csv \
  --target_col target \
  --task_type regression \
  --n_real 50 \
  --final_samples 500 \
  --device cuda
```

## **Citation**

If you found the resources in this repository useful, please cite our work:

```bibtex
@misc{zhang2026tap,
      title={Active Tabular Augmentation via Policy-Guided Diffusion Inpainting}, 
      author={Zheyu Zhang and Shuo Yang and Bardh Prenkaj and Gjergji Kasneci},
      year={2026},
      eprint={2605.10315},
      archivePrefix={arXiv},
      primaryClass={cs.LG},
      url={https://arxiv.org/abs/2605.10315}, 
}
```

