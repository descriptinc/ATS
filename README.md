# Goodbye Drift: Anchored Tree Sampling for Long-Horizon Video-to-Video Generation

<p align="center">
  Matthew Bendel &middot; Stephen W. Bailey &middot; Mithilesh Vaidya &middot; Sumukh Badam &middot; Xingzhe He
</p>

<p align="center">
  <b>Descript, Inc.</b>
</p>

[![Paper](https://img.shields.io/badge/ArXiv-2605.20476-red)](https://arxiv.org/abs/2605.20476)
[![Project Page](https://img.shields.io/badge/Project-Page-blue)](https://descriptinc.github.io/ATS/)
[![Code](https://img.shields.io/badge/GitHub-Coming_Soon-lightgrey)](#)

## Abstract

Long-horizon video generation suffers from two intertwined issues. First, there is **drift**, where video quality degrades over time. Second, there are **continuity** issues, which manifest as object permanence failures or improperly rendered transient content (e.g., an object that appears in non-consecutive frames changing color or style). Recent work has focused on autoregressive distillation techniques that attack both problems simultaneously. We instead choose to focus on drift directly and introduce **Anchored Tree Sampling (ATS)**: a training-free, inference-time scheduler that replaces left-to-right rollout with sparse-to-dense, anchor-bounded imputation organized as a tree. A root call produces sparse anchors over the full horizon, recursive refinement generates intermediate anchors, and final leaf spans are synthesized between neighboring anchors. This reduces the critical path from $K$ sequential rollout steps to $L+1$ tree-hierarchical steps and converts horizon-compounding drift into anchor-bounded drift. We focus on V2V generation in the *static-camera* regime, where sparse anchors over the horizon are well approximated by the dense conditioning signal, and the base model can produce them without retraining. We evaluate ATS against two contemporary autoregressive baselines on Wan&nbsp;2.1&nbsp;+&nbsp;VACE, across five conditioning modalities (inpainting, outpainting, edge, pose, depth). We show that ATS outperforms both competitors in overall quality, as well as in drift prevention. We additionally demonstrate stable &geq;&nbsp;40-minute generation on LTX-2.3 across the same five modalities. We conclude by proposing a path forward to extend ATS to arbitrarily long T2V generation, as well as the dynamic-camera and multi-shot regimes.

## Code

Code coming soon.

## Citation

```bibtex
@misc{bendel2026goodbyedriftanchoredtree,
      title={Goodbye Drift: Anchored Tree Sampling for Long-Horizon Video-to-Video Generation}, 
      author={Matthew Bendel and Stephen W. Bailey and Mithilesh Vaidya and Sumukh Badam and Xingzhe He},
      year={2026},
      eprint={2605.20476},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2605.20476}, 
}
```
