<h1 align="center">Tabular Augmentation Policy</h1>

<p align="center">
Initial code release for the paper [ICML 2026] [Active Tabular Augmentation via Policy-Guided Diffusion Inpainting](https://arxiv.org/abs/2605.10315).
</p>


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

