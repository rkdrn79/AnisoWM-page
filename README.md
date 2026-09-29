<div align="center">

# Anisotropic Representations Improve Planning in JEPA World Models

**Mingu Kang**<sup>1</sup>, **Yoori Oh**<sup>1†</sup>, **Sookyung Kim**<sup>2†</sup>, **Joonseok Lee**<sup>1†</sup>

<sup>1</sup>Seoul National University &nbsp;&nbsp; <sup>2</sup>Ewha Womans University &nbsp;&nbsp; <sup>†</sup>Corresponding authors

[![Project Page](https://img.shields.io/badge/Project-Page-blue)](https://rkdrn79.github.io/AnisoWM-page/)
[![Paper](https://img.shields.io/badge/Paper-PDF-b31b1b)](https://rkdrn79.github.io/AnisoWM-page/static/AnisoWM_preprint.pdf)

</div>

<p align="center">
  <img src="static/figures/fig_main_result_full.png" width="90%" alt="Planning success across four environments">
</p>

## Summary

Latent world models such as LeWM rank candidate actions by the Euclidean distance between a predicted representation and a goal representation. The isotropic Gaussian regularizer (SIGReg) that prevents collapse also fixes how terminal errors are weighted during planning. We show that **accurate prediction and noncollapsed representations do not guarantee a task-aligned planning cost**: isotropic regularization can make the planner rank reachable outcomes differently from the task cost.

**AnisoWM** with **ΛReg** replaces the fixed isotropic target with a **learnable diagonal covariance** under fixed-trace and condition-number (κ) constraints. The prediction objective, predictor architecture and Euclidean planner stay the same, and the target is used only during training.

With a single shared bound κ = 2, AnisoWM plans more successfully than LeWM in all four environments:

| Environment | LeWM | AnisoWM (Ours) |
|---|:-:|:-:|
| Two-Room | 87 | **93** |
| Reacher | 86 | **89** |
| Push-T | 96 | **97** |
| OGBench-Cube | 74 | **79** |

Success rate (%), mean over three training seeds.

## Rollouts

LeWM and AnisoWM start from the same initial state, with the same goal, CEM planner and random seed. See the [project page](https://rkdrn79.github.io/AnisoWM-page/) for rollout videos in all four environments.

## Citation

```bibtex
@misc{kang2026anisowm,
  title  = {Anisotropic Representations Improve Planning in JEPA World Models},
  author = {Kang, Mingu and Oh, Yoori and Kim, Sookyung and Lee, Joonseok},
  year   = {2026},
  note   = {Preprint}
}
```

## Acknowledgements

The page template is adapted from [Nerfies](https://github.com/nerfies/nerfies.github.io).
