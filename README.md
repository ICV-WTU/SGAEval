# SGAEval

**Satellite-Guided Assessment of Structural Distortion in SLAM Point Cloud Maps**

This repository contains the static project website for SGAEval. It presents a method for assessing structural distortion in outdoor SLAM point cloud maps using satellite imagery or aerial orthophotos, along with the dataset and experimental results.

## Overview

The website introduces **MLSD (Maximum Local Scale Deviation)**, a weak-reference metric for evaluating structural distortion in SLAM maps. It aligns the horizontal projection of a point cloud map with an overhead reference image and measures local scale changes in the fitted transformation, without requiring dense 3D ground-truth point clouds.

The page includes:

- An introduction to MLSD and its evaluation pipeline;
- Details of the self-collected Campus and Road outdoor LiDAR sequences from Wuhan Textile University and its surroundings;
- Qualitative visualizations and quantitative results for Backpack2025 Seq.2, Campus, and Road;
- Links to the dataset and source-code repository, plus a BibTeX citation.

## Project Links

- Dataset: [SGAEval Dataset](https://opendatalab.org.cn/ICVGroup-WTU/SGAEval-DATASET/tree/main)
- Source code: [SGAEval on GitHub](https://github.com/ICV-WTU/SGAEval-Satellite-Guided-Assessment-of-Structural-Distortion-in-SLAM-Point-Cloud-Maps)

## Directory Structure

```text
.
├── index.html            # Website page, including styles and carousel scripts
└── static/
    └── images/           # Method, dataset, qualitative-result, and demo assets
```

## Local Preview

This is a static website and does not require dependencies or a build step. Open `index.html` directly, or start a local HTTP server from the project root:

```bash
python -m http.server 8000
```

Then open <http://localhost:8000> in a browser.

## Deployment

The website can be deployed to any static hosting service. For GitHub Pages, select the branch and directory containing `index.html` as the publishing source. No build command is needed.

## Updating the Website

- Edit `index.html` to update the project description, results, or citation.
- Add or replace images in `static/images/` and update the corresponding paths in `index.html`.
- To update the results carousel, change the `src` attributes of its `<img>` elements in `index.html`. All three carousel slides currently point to `static/images/SGASD_.gif`; replace them with the appropriate assets to show different results.
- After the paper is published, replace the `Paper` button's placeholder URL (`#`) at the top of the page with the paper link.

## Citation

```bibtex
@article{ma2026sgaeval,
  title   = {SGAEval: Satellite-Guided Assessment of Structural Distortion in SLAM Point Cloud Maps},
  author  = {Ma, Yunfei and Zou, Gan and Cheng, Jun},
  journal = {Preprint submitted to IEEE},
  year    = {2026}
}
```
