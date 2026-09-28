# CALIMAP

### CALIMAP: Plug-and-Play Query Adaptation for Robust Vectorized HD Map Construction

**Accepted at ACCV 2026**

CALIMAP is a plug-and-play adaptation framework for robust online vectorized HD map construction under camera-LiDAR misalignment.

The framework adapts both the decoder query and the fused BEV representation while preserving the pretrained map constructor.  
Biased Query Modulation (BQM) incorporates camera-LiDAR context into the shared map query and generates alignment-biased and mapping-biased queries.  
Implicit BEV Alignment (IBA) uses the alignment-biased query to adjust the fused BEV representation, while the mapping-biased query is used for map prediction.  
Query-Guided Aggregation (QGA) provides lightweight context aggregation in both BQM and IBA.

<p align="center">
  <img src="assets/overview.png" width="90%">
</p>

## Method Overview

<p align="center">
  <img src="fig/bqm.png" width="90%">
</p>

CALIMAP keeps the pretrained encoder, decoder, and prediction head frozen and trains only the adapter modules and shared query.

## Qualitative Results

<p align="center">
  <img src="fig/qualitative_results.png" width="90%">
</p>

## Code

The code is currently being cleaned and organized for public release.  
The official implementation will be released in this repository.

## Citation

If you find this work useful, please consider citing:

```bibtex
@inproceedings{
kim2026calimap,
title={{CALIMAP}: Plug-and-Play Query Adaptation for Robust Vectorized {HD} Map Construction},
author={Juyoung Kim and Ji-Hong Park and Sang-Min Choi and Gun-Woo Kim},
booktitle={Eighteenth Asian Conference on Computer Vision},
year={2026},
url={https://openreview.net/forum?id=JzMRYM38s8}
}
