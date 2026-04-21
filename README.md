# Awesome Feed-Forward 3D

[![Paper](https://img.shields.io/badge/Paper-arXiv%3A2604.14025-B31B1B?style=flat-square&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2604.14025)
[![Website](https://img.shields.io/badge/Website-ff3d--survey.github.io-blue?style=flat-square)](https://ff3d-survey.github.io/)
[![GitHub](https://img.shields.io/badge/GitHub-ziplab%2FAwesome--Feed--Forward--3D-black?style=flat-square&logo=github)](https://github.com/ziplab/Awesome-Feed-Forward-3D)

An curated list for feed-forward 3D scene modeling, including research directions, datasets, and applications.

| <img width="100%" src="https://ff3d-survey.github.io/assets/overview.png"> |
|:-:|

## Table of Contents

- [Research Directions](#directions)
  - [Feature Enhancement](#feature-enhancement)
    - [Advanced Encoding Architectures](#advanced-encoding-architectures)
    - [Cross-View Fusion](#cross-view-fusion)
    - [Integration of Visual Foundation Models](#integration-of-visual-foundation-models)
  - [Geometry-aware Improvement](#geometry-aware-improvement)
    - [Explicit Geometric Aggregation](#explicit-geometric-aggregation)
    - [Refining Predicted 3D Scenes](#refining-predicted-3d-scenes)
    - [Pose-Free Reconstruction](#pose-free-reconstruction)
    - [Pre-trained Geometric Guidance](#pre-trained-geometric-guidance)
  - [Model Efficiency](#model-efficiency)
    - [Feature Efficiency](#feature-efficiency)
    - [Representation Compaction](#representation-compaction)
  - [Data & Visual Augmentation](#data--visual-augmentation)
    - [Data Augmentation](#data-augmentation)
    - [Visual Augmentation](#visual-augmentation)
  - [Temporal-aware Models](#temporal-aware-models)
    - [Online Streaming](#online-streaming)
    - [Offline Processing](#offline-processing)
    - [Interactive Modeling](#interactive-modeling)
    - [Specialized Tasks](#specialized-tasks)
- [Datasets and Benchmarks](#datasets)
  - [Geometry Oriented](#geometry-oriented)
  - [Visual Oriented](#visual-oriented)
  - [Mixed](#mixed)
- [Applications](#application)
  - [Autonomous Driving](#autonomous-driving)
  - [Robotics](#robotics)
  - [SfM & SLAM](#sfm--slam)
  - [Scene Understanding](#scene-understanding)
  - [Video Generation](#video-generation)
  - [Others](#others)

## Taxonomy

| <img width="100%" src="https://ff3d-survey.github.io/assets/taxonomy.png"> |
|:-:|

## Research Directions

## Feature Enhancement

### Advanced Encoding Architectures

- pixelNeRF: Neural Radiance Fields from One or Few Images. [[:page_facing_up: Paper](https://arxiv.org/abs/2012.02190) | [:computer: Code](https://github.com/sxyu/pixel-nerf)]
- IBRNet: Learning Multi-View Image-Based Rendering. [[:page_facing_up: Paper](https://arxiv.org/abs/2102.13090) | [:computer: Code](https://github.com/googleinterns/IBRNet)｜[:globe_with_meridians: Project Page](https://ibrnet.github.io/)]
- Splatter Image: Ultra-Fast Single-View 3D Reconstruction. [[:page_facing_up: Paper](https://robots.ox.ac.uk/~vgg/publications/2024/Szymanowicz24/szymanowicz24.pdf) | [:computer: Code](https://github.com/szymanowiczs/splatter-image)｜[:globe_with_meridians: Project Page](https://szymanowiczs.github.io/splatter-image)]
- Convolutional Occupancy Networks. [[:page_facing_up: Paper](https://arxiv.org/abs/2003.04618) | [:computer: Code](https://github.com/autonomousvision/convolutional_occupancy_networks)｜[:globe_with_meridians: Project Page](https://pengsongyou.github.io/conv_onet)]
- Light Field Networks: Neural Scene Representations with Single-Evaluation Rendering. [[:page_facing_up: Paper](https://arxiv.org/abs/2106.02634) | [:computer: Code](https://github.com/vsitzmann/light-field-networks)｜[:globe_with_meridians: Project Page](https://vsitzmann.github.io/lfns/)]
- Learned Initializations for Optimizing Coordinate-Based Neural Representations. [[:page_facing_up: Paper](https://arxiv.org/abs/2012.02189) | [:computer: Code](https://github.com/tancik/learnit)｜[:globe_with_meridians: Project Page](https://www.matthewtancik.com/learnit)]
- Neural Rays for Occlusion-aware Image-based Rendering. [[:page_facing_up: Paper](https://arxiv.org/abs/2107.13421) | [:computer: Code](https://github.com/liuyuan-pal/NeuRay)｜[:globe_with_meridians: Project Page](https://liuyuan-pal.github.io/NeuRay/)]
- ${C}^{3}$-GS: Learning Context-aware, Cross-dimension, Cross-scale Feature for Generalizable Gaussian Splatting. [[:page_facing_up: Paper](https://arxiv.org/abs/2508.20754) | [:computer: Code](https://github.com/YuhsiHu/C3-GS)]
- Scene Representation Transformer: Geometry-Free Novel View Synthesis Through Set-Latent Scene Representations. [[:page_facing_up: Paper](https://arxiv.org/abs/2111.13152) | [:computer: Code](https://github.com/stelzner/srt)｜[:globe_with_meridians: Project Page](https://srt-paper.github.io/)]
- VisionNeRF: Vision Transformer for NeRF-Based View Synthesis from a Single Input Image. [[:page_facing_up: Paper](https://arxiv.org/abs/2207.05736) | [:computer: Code](https://github.com/ken2576/vision-nerf)｜[:globe_with_meridians: Project Page](https://cseweb.ucsd.edu/~viscomp/projects/VisionNeRF/)]
- RePAST: Relative Pose Attention Scene Representation Transformer. [[:page_facing_up: Paper](https://arxiv.org/abs/2304.00947)]
- Is Attention All That NeRF Needs? [[:page_facing_up: Paper](https://arxiv.org/abs/2207.13298) | [:computer: Code](https://github.com/VITA-Group/GNT)｜[:globe_with_meridians: Project Page](https://vita-group.github.io/GNT/)]
- Large Reconstruction Model (LRM).
- Instant3D: Fast Text-to-3D with Sparse-view Generation and Large Reconstruction Model.
- TripoSR: Fast 3D Object Reconstruction from a Single Image. [[:page_facing_up: Paper](https://arxiv.org/abs/2403.02151)]
- GRM: Large Gaussian Reconstruction Model for Efficient 3D Reconstruction and Generation.
- GS-LRM: Large Reconstruction Model for 3D Gaussian Splatting. [[:page_facing_up: Paper](https://arxiv.org/abs/2403.14621) | [:computer: Code](https://github.com/imlixinyang/GS-LRM)｜[:globe_with_meridians: Project Page](https://sai-bi.github.io/project/gs-lrm/)]
- MeshLRM: Large Reconstruction Model for High-Quality Meshes.
- MeshFormer: High-Quality Mesh Generation with 3D-Guided Reconstruction Model.
- Flex3D: Feed-Forward 3D Generation With Flexible Reconstruction Model And Input View Curation.
- LVSM: A Fully Data-Driven Approach to Novel View Synthesis.
- Depth Anything 3: Recovering the Visual Space from Any Views.
- Gamba: Marry Gaussian Splatting With Mamba for Single-View 3D Reconstruction.
- MVGamba: Unify 3D Content Generation as State Space Sequence Modeling.
- Long-LRM: Long-sequence Large Reconstruction Model for Wide-coverage Gaussian Splats. [[:page_facing_up: Paper](https://arxiv.org/abs/2410.12781) | [:computer: Code](https://github.com/arthurhero/Long-LRM)｜[:globe_with_meridians: Project Page](https://arthurhero.github.io/projects/llrm/)]

### Cross-View Fusion

- AttnRend: Learning to Render Novel Views from Wide-Baseline Stereo Pairs. [[:page_facing_up: Paper](https://arxiv.org/abs/2304.08463) | [:computer: Code](https://github.com/yilundu/cross_attention_renderer)｜[:globe_with_meridians: Project Page](https://yilundu.github.io/wide_baseline/)]
- Epipolar-Free 3D Gaussian Splatting for Generalizable Novel View Synthesis. [[:page_facing_up: Paper](https://arxiv.org/abs/2404.06109) | [:computer: Code](https://github.com/tatakai1/eFreeSplat)｜[:globe_with_meridians: Project Page](https://tatakai1.github.io/efreesplat/)]
- LGM: Large Multi-View Gaussian Model for High-Resolution 3D Content Creation.
- DUSt3R: Geometric 3D Vision Made Easy. [[:page_facing_up: Paper](https://arxiv.org/abs/2312.14132) | [:computer: Code](https://github.com/naver/dust3r)｜[:globe_with_meridians: Project Page](https://dust3r.europe.naverlabs.com/)]
- Grounding Image Matching in 3D with MASt3R. [[:page_facing_up: Paper](https://arxiv.org/abs/2406.09756) | [:computer: Code](https://github.com/naver/mast3r)｜[:globe_with_meridians: Project Page](https://europe.naverlabs.com/blog/mast3r-matching-and-stereo-3d-reconstruction/)]
- MV-DUSt3R: Multi-View Dense Stereo 3D Reconstruction.
- MV-DUSt3R+: Single-Stage Scene Reconstruction from Sparse Views In 2 Seconds. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.06974) | [:computer: Code](https://github.com/facebookresearch/mvdust3r)｜[:globe_with_meridians: Project Page](https://mv-dust3rp.github.io/)]
- PreF3R: Pose-Free Feed-Forward 3D Gaussian Splatting from Variable-length Image Sequence. [[:page_facing_up: Paper](https://arxiv.org/abs/2411.16877) | [:computer: Code](https://github.com/ComputationalRobotics/PreF3R)｜[:globe_with_meridians: Project Page](https://computationalrobotics.seas.harvard.edu/PreF3R/)]
- 3D Reconstruction with Spatial Memory. [[:page_facing_up: Paper](https://arxiv.org/abs/2408.16061) | [:computer: Code](https://github.com/HengyiWang/spann3r)｜[:globe_with_meridians: Project Page](https://hengyiwang.github.io/projects/spanner)]
- Fast3R: Towards 3D Reconstruction of 1000+ Images in One Forward Pass. [[:page_facing_up: Paper](https://arxiv.org/abs/2501.13928) | [:computer: Code](https://github.com/facebookresearch/fast3r)｜[:globe_with_meridians: Project Page](https://fast3r-3d.github.io/)]
- MUSt3R: Multi-view Network for Stereo 3D Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2503.01661) | [:computer: Code](https://github.com/naver/must3r)｜[:globe_with_meridians: Project Page](https://europe.naverlabs.com/research/publications/must3r-multi-view-network-for-stereo-3d-reconstruction/)]
- WinT3R: Window-Based Streaming Reconstruction with Camera Token Pool. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.05296)]
- Continuous 3D Perception Model with Persistent State. [[:page_facing_up: Paper](https://arxiv.org/abs/2501.12387) | [:computer: Code](https://github.com/CUT3R/CUT3R)｜[:globe_with_meridians: Project Page](https://cut3r.github.io/)]
- VolSplat: Rethinking Feed-Forward 3D Gaussian Splatting with Voxel-Aligned Prediction. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.19297)]
- G-CUT3R: Guided 3D Reconstruction with Camera and Depth Prior Integration. [[:page_facing_up: Paper](https://arxiv.org/abs/2508.11379)]
- TTT3R: 3D Reconstruction as Test-Time Training. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.26645)]
- Point3R: Streaming 3D Reconstruction with Explicit Spatial Pointer Memory. [[:page_facing_up: Paper](https://arxiv.org/abs/2507.02863)]
- VGGT: Visual Geometry Grounded Transformer. [[:page_facing_up: Paper](https://arxiv.org/abs/2503.11651) | [:computer: Code](https://github.com/facebookresearch/vggt)｜[:globe_with_meridians: Project Page](https://vgg-t.github.io/)]
- iLRM: An Iterative Large 3D Reconstruction Model. [[:page_facing_up: Paper](https://arxiv.org/abs/2507.23277) | [:computer: Code](https://github.com/Gynjn/iLRM)｜[:globe_with_meridians: Project Page](https://gynjn.github.io/iLRM/)]
- Dens3r: A Foundation Model for 3D Geometry Prediction. [[:page_facing_up: Paper](https://arxiv.org/abs/2507.16290)]
- MoRE: 3D Visual Geometry Reconstruction Meets Mixture-of-Experts. [[:page_facing_up: Paper](https://arxiv.org/abs/2510.27234)]
- Uni3R: Unified 3D Reconstruction and Semantic Understanding via Generalizable Gaussian Splatting from Unposed Multi-view Images. [[:page_facing_up: Paper](https://arxiv.org/abs/2508.03643)]
- Flow3r: Factored Flow Prediction for Scalable Visual Geometry Learning. [[:page_facing_up: Paper](https://arxiv.org/abs/2602.20157)]
- Gen3R: 3D Scene Generation Meets Feed-Forward Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2601.04090)]
- NOVA3R: Non-pixel-aligned Visual Transformer for Amodal 3D Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2603.04179) | [:computer: Code](https://github.com/wrchen530/nova3r)｜[:globe_with_meridians: Project Page](https://wrchen530.github.io/nova3r/)]
- IncVGGT: Incremental VGGT for Memory-Bounded Long-Range 3D Reconstruction.
- ZipMap: Linear-Time Stateful 3D Reconstruction with Test-Time Training. [[:page_facing_up: Paper](https://arxiv.org/abs/2603.04385)]
- LoGeR: Long-Context Geometric Reconstruction with Hybrid Memory. [[:page_facing_up: Paper](https://arxiv.org/abs/2603.03269)]
- tttLRM: Test-Time Training for Long Context and Autoregressive 3D Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2602.20160)]
- VGG-T3: Offline Feed-Forward 3D Reconstruction at Scale. [[:page_facing_up: Paper](https://arxiv.org/abs/2602.23361)]

### Integration of Visual Foundation Models

- DUSt3R: Geometric 3D Vision Made Easy. [[:page_facing_up: Paper](https://arxiv.org/abs/2312.14132) | [:computer: Code](https://github.com/naver/dust3r)｜[:globe_with_meridians: Project Page](https://dust3r.europe.naverlabs.com/)]
- Mono3R: Exploiting Monocular Cues for Geometric 3D Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2504.13419)]
- Feat2GS: Probing Visual Foundation Models with Gaussian Splatting. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.09606) | [:computer: Code](https://github.com/fanegg/Feat2GS)｜[:globe_with_meridians: Project Page](https://fanegg.github.io/Feat2GS/)]
- CATSplat: Context-Aware Transformer with Spatial Guidance for Generalizable 3D Gaussian Splatting from A Single-View Image. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.12906)]

## Geometry-aware Improvement

### Explicit Geometric Aggregation

- MVSNeRF: Fast Generalizable Radiance Field Reconstruction from Multi-View Stereo. [[:page_facing_up: Paper](https://arxiv.org/abs/2103.15595) | [:computer: Code](https://github.com/apchenstu/mvsnerf)｜[:globe_with_meridians: Project Page](https://apchenstu.github.io/mvsnerf/)]
- Stereo Radiance Fields (SRF): Learning View Synthesis for Sparse Views of Novel Scenes. [[:page_facing_up: Paper](https://arxiv.org/abs/2104.06935) | [:computer: Code](https://github.com/jchibane/srf)｜[:globe_with_meridians: Project Page](https://virtualhumans.mpi-inf.mpg.de/srf/)]
- GeoNeRF: Generalizing NeRF with Geometry Priors. [[:page_facing_up: Paper](https://arxiv.org/abs/2111.13539) | [:computer: Code](https://github.com/idiap/GeoNeRF)｜[:globe_with_meridians: Project Page](https://www.idiap.ch/paper/geonerf/)]
- BoostMVSNeRFs: Boosting MVS-based NeRFs to Generalizable View Synthesis in Large-Scale Scenes.
- Generalizable Patch-Based Neural Rendering. [[:page_facing_up: Paper](https://arxiv.org/abs/2207.10662) | [:computer: Code](https://github.com/google-research/google-research/tree/master/gen_patch_neural_rendering)｜[:globe_with_meridians: Project Page](https://mohammedsuhail.net/gen_patch_neural_rendering/)]
- MatchNeRF: Explicit Correspondence Matching for Generalizable Neural Radiance Fields. [[:page_facing_up: Paper](https://arxiv.org/abs/2304.12294) | [:computer: Code](https://github.com/donydchen/matchnerf)｜[:globe_with_meridians: Project Page](https://donydchen.github.io/matchnerf)]
- GTA: A Geometry-Aware Attention Mechanism for Multi-View Transformers. [[:page_facing_up: Paper](https://arxiv.org/abs/2310.10375) | [:computer: Code](https://github.com/autonomousvision/gta)｜[:globe_with_meridians: Project Page](https://takerum.github.io/gta/)]
- MuRF: Multi-Baseline Radiance Fields. [[:page_facing_up: Paper](https://arxiv.org/abs/2312.04565) | [:computer: Code](https://github.com/autonomousvision/murf)｜[:globe_with_meridians: Project Page](https://haofeixu.github.io/murf/)]
- SparseNeuS: Fast Generalizable Neural Surface Reconstruction from Sparse Views.
- VolRecon: Volume Rendering of Signed Ray Distance Functions for Generalizable Multi-View Reconstruction.
- ReTR: Modeling Depth Distribution for Generalizable Surface Reconstruction.
- UFORecon: Generalizable Sparse-View Surface Reconstruction from Arbitrary and Unfavorable Sets.
- SurfaceSplat: Connecting Surface Reconstruction and Gaussian Splatting. [[:page_facing_up: Paper](https://arxiv.org/abs/2507.15602)]
- RenderFormer: Transformer-based Neural Rendering of Triangle Meshes with Global Illumination. [[:page_facing_up: Paper](https://arxiv.org/abs/2505.21925) | [:computer: Code](https://github.com/microsoft/renderformer)｜[:globe_with_meridians: Project Page](https://microsoft.github.io/renderformer/)]
- AGG: Amortized Generative 3D Gaussians for Single Image to 3D. [[:page_facing_up: Paper](https://arxiv.org/abs/2401.04099)]
- TGS: Triplane Meets Gaussian Splatting: Fast and Generalizable Single-View 3D Reconstruction with Transformers.
- LaRa: Efficient Large-Baseline Radiance Fields. [[:page_facing_up: Paper](https://arxiv.org/abs/2407.04699) | [:computer: Code](https://github.com/autonomousvision/LaRa)｜[:globe_with_meridians: Project Page](https://apchenstu.github.io/LaRa/)]
- MeshSplat: Generalizable Sparse-View Surface Reconstruction via Gaussian Splatting. [[:page_facing_up: Paper](https://arxiv.org/abs/2508.17811)]
- TranSplat: Geometry-Aware Feed-Forward Gaussian Splatting with Transformation Consistency.
- H3R: Hybrid Multi-view Correspondence for Generalizable 3D Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2508.03118)]
- MuGS: Multi-Baseline Generalizable Gaussian Splatting Reconstruction.
- pixelSplat: 3D Gaussian Splats from Image Pairs for Scalable Generalizable 3D Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2312.12337) | [:computer: Code](https://github.com/dcharatan/pixelsplat)｜[:globe_with_meridians: Project Page](https://dcharatan.github.io/pixelsplat)]
- MVSplat: Efficient 3D Gaussian Splatting from Sparse Multi-View Images. [[:page_facing_up: Paper](https://arxiv.org/abs/2403.14627) | [:computer: Code](https://github.com/donydchen/mvsplat)｜[:globe_with_meridians: Project Page](https://donydchen.github.io/mvsplat)]
- MVSGaussian: Fast Generalizable Gaussian Splatting Reconstruction from Multi-View Stereo. [[:page_facing_up: Paper](https://arxiv.org/abs/2501.15364) | [:computer: Code](https://github.com/TQTQliu/MVSGaussian)｜[:globe_with_meridians: Project Page](https://mvsgaussian.github.io/)]

### Refining Predicted 3D Scenes

- FreeSplat: Generalizable 3D Gaussian Splatting Towards Free-View Synthesis of Indoor Scenes. [[:page_facing_up: Paper](https://arxiv.org/abs/2405.17958) | [:computer: Code](https://github.com/wangys16/FreeSplat)｜[:globe_with_meridians: Project Page](https://wangys16.github.io/FreeSplat-project/)]
- HiSplat: Hierarchical 3D Gaussian Splatting for Generalizable Sparse-View Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2410.06245) | [:computer: Code](https://github.com/Open3DVLab/HiSplat)｜[:globe_with_meridians: Project Page](https://open3dvlab.github.io/HiSplat/)]
- PixelGaussian: Generalizable 3D Gaussian Reconstruction from Arbitrary Views. [[:page_facing_up: Paper](https://arxiv.org/abs/2410.18979) | [:computer: Code](https://github.com/Barrybarry-Smith/PixelGaussian)｜[:globe_with_meridians: Project Page](https://wzzheng.net/PixelGaussian)]
- Gaussian Graph Network: Learning Efficient and Generalizable Gaussian Representations from Multi-view Images. [[:page_facing_up: Paper](https://arxiv.org/abs/2503.16338) | [:computer: Code](https://github.com/shengjun-zhang/GGN)｜[:globe_with_meridians: Project Page](https://shengjun-zhang.github.io/GGN/)]
- Generative Densification: Learning to Densify Gaussians for High-Fidelity Generalizable 3D Reconstruction.
- G3R: Gradient Guided Generalizable Reconstruction.

### Pose-Free Reconstruction

- LEAP: Liberate Sparse-view 3D Modeling from Camera Poses. [[:page_facing_up: Paper](https://arxiv.org/abs/2310.01410) | [:computer: Code](https://github.com/hwjiang1510/LEAP)｜[:globe_with_meridians: Project Page](https://hwjiang1510.github.io/LEAP/)]
- Splatt3R: Zero-shot Gaussian Splatting from Uncalibrated Image Pairs. [[:page_facing_up: Paper](https://arxiv.org/abs/2408.13912) | [:computer: Code](https://github.com/btsmart/splatt3r)｜[:globe_with_meridians: Project Page](https://splatt3r.active.vision/)]
- No Pose, No Problem: Surprisingly Simple 3D Gaussian Splats from Sparse Unposed Images. [[:page_facing_up: Paper](https://arxiv.org/abs/2410.24207) | [:computer: Code](https://github.com/cvg/NoPoSplat)｜[:globe_with_meridians: Project Page](https://noposplat.github.io/)]
- PF3plat: Pose-Free Feed-Forward 3D Gaussian Splatting. [[:page_facing_up: Paper](https://arxiv.org/abs/2410.22128) | [:computer: Code](https://cvlab-kaist.github.io/PF3plat/)｜[:globe_with_meridians: Project Page](https://cvlab-kaist.github.io/PF3plat/)]
- FreeSplatter: Pose-free Gaussian Splatting for Sparse-view 3D Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.09573) | [:computer: Code](https://github.com/TencentARC/FreeSplatter)]
- FLARE: Feed-forward Geometry, Appearance and Camera Estimation from Uncalibrated Sparse Views. [[:page_facing_up: Paper](https://arxiv.org/abs/2502.12138) | [:computer: Code](https://github.com/ant-research/FLARE)｜[:globe_with_meridians: Project Page](https://zhanghe3z.github.io/FLARE/)]
- Pow3R: Empowering Unconstrained 3D Reconstruction with Camera and Scene Priors. [[:page_facing_up: Paper](https://arxiv.org/abs/2503.17316) | [:computer: Code](https://github.com/naver/pow3r)｜[:globe_with_meridians: Project Page](https://europe.naverlabs.com/research/publications/pow3r-empowering-unconstrained-3d-reconstruction-with-camera-and-scene-priors/)]
- RegGS: Unposed Sparse Views Gaussian Splatting with 3DGS Registration. [[:page_facing_up: Paper](https://arxiv.org/abs/2507.08136) | [:computer: Code](https://github.com/3DAgentWorld/RegGS)｜[:globe_with_meridians: Project Page](https://3dagentworld.github.io/reggs/)]
- UFV-Splatter: Pose-Free Feed-Forward 3D Gaussian Splatting Adapted to Unfavorable Views. [[:page_facing_up: Paper](https://arxiv.org/abs/2507.22342) | [:computer: Code](https://github.com/yfujimura/UFV-Splatter/)｜[:globe_with_meridians: Project Page](https://yfujimura.github.io/UFV-Splatter_page)]
- π^3: Scalable Permutation-Equivariant Visual Geometry Learning. [[:page_facing_up: Paper](https://arxiv.org/abs/2507.13347) | [:computer: Code](https://github.com/yyfz/Pi3)｜[:globe_with_meridians: Project Page](https://yyfz.github.io/pi3/)]
- AnySplat: Feed-forward 3D Gaussian Splatting from Unconstrained Views. [[:page_facing_up: Paper](https://arxiv.org/abs/2505.23716)]
- No Pose at All: Self-Supervised Pose-Free 3D Gaussian Splatting from Sparse Views.
- SPFSplatV2: Efficient Self-Supervised Pose-Free 3D Gaussian Splatting from Sparse Views. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.17246)]
- PLANA3R: Zero-shot Metric Planar 3D Reconstruction via Feed-forward Planar Splatting.
- YoNoSplat: You Only Need One Model for Feedforward 3D Gaussian Splatting. [[:page_facing_up: Paper](https://arxiv.org/abs/2511.07321)]

### Pre-trained Geometric Guidance

- DepthSplat: Connecting Gaussian Splatting and Depth. [[:page_facing_up: Paper](https://arxiv.org/abs/2410.13862) | [:computer: Code](https://github.com/cvg/depthsplat)｜[:globe_with_meridians: Project Page](https://haofeixu.github.io/depthsplat/)]
- Flash3D: Feed-Forward Generalisable 3D Scene Reconstruction from a Single Image. [[:page_facing_up: Paper](https://arxiv.org/abs/2406.04343) | [:computer: Code](https://github.com/eldar/flash3d)｜[:globe_with_meridians: Project Page](https://www.robots.ox.ac.uk/~vgg/research/flash3d/)]
- Niagara: Normal-Integrated Geometric Affine Field for Scene Reconstruction from a Single View. [[:page_facing_up: Paper](https://arxiv.org/abs/2503.12553) | [:computer: Code](https://github.com/xianzuwu/Niagara)｜[:globe_with_meridians: Project Page](https://ai-kunkun.github.io/Niagara_page/)]
- Revisiting Depth Representations for Feed-Forward 3D Gaussian Splatting. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.05327) | [:computer: Code](https://github.com/aim-uofa/PM-Loss)｜[:globe_with_meridians: Project Page](https://aim-uofa.github.io/PMLoss/)]
- Fin3R: Fine-tuning Feed-forward 3D Reconstruction Models via Monocular Knowledge Distillation. [[:page_facing_up: Paper](https://arxiv.org/abs/2511.22429)]
- JointSplat: Joint Depth and Flow Priors for Feed-Forward 3D Gaussian Splatting. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.03872)]

## Model Efficiency

### Feature Efficiency

- Efficient Neural Radiance Fields for Interactive Free-viewpoint Video. [[:page_facing_up: Paper](https://arxiv.org/abs/2304.04452) | [:computer: Code](https://github.com/aoliao12138/ReRF)｜[:globe_with_meridians: Project Page](https://aoliao12138.github.io/ReRF/)]
- ProNeRF: Learning Efficient Projection-Aware Ray Sampling for Fine-Grained Implicit Neural Radiance Fields. [[:page_facing_up: Paper](https://arxiv.org/abs/2312.08136) | [:computer: Code](https://github.com/KAIST-VICLab/pronerf)｜[:globe_with_meridians: Project Page](https://kaist-viclab.github.io/pronerf-site/)]
- TinySplat: Feedforward Approach for Generating Compact 3D Scene Representation. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.09479)]
- ZPressor: Bottleneck-Aware Compression for Scalable Feed-Forward 3DGS. [[:page_facing_up: Paper](https://arxiv.org/abs/2505.23734) | [:computer: Code](https://github.com/ziplab/ZPressor)｜[:globe_with_meridians: Project Page](https://lhmd.top/zpressor/)]
- FastVGGT: Training-Free Acceleration of Visual Geometry Transformer. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.02560) | [:computer: Code](https://github.com/mystorm16/FastVGGT)｜[:globe_with_meridians: Project Page](https://mystorm16.github.io/fastvggt/)]
- Quantized Visual Geometry Grounded Transformer. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.21302)]
- Faster VGGT with Block-Sparse Global Attention. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.07120)]
- Evict3R: Training-Free Token Eviction for Memory-Bounded Streaming Visual Geometry Transformers. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.17650)]
- LiteVGGT: Boosting Vanilla VGGT via Geometry-aware Cached Token Merging. [[:page_facing_up: Paper](https://arxiv.org/abs/2512.04939)]
- Speed3R: Sparse Feed-forward 3D Reconstruction Models. [[:page_facing_up: Paper](https://arxiv.org/abs/2603.08055)]
- SR3R: Rethinking Super-Resolution 3D Reconstruction With Feed-Forward Gaussian Splatting. [[:page_facing_up: Paper](https://arxiv.org/abs/2602.24020)]

### Representation Compaction

- Gaussian Graph Network: Learning Efficient and Generalizable Gaussian Representations from Multi-view Images. [[:page_facing_up: Paper](https://arxiv.org/abs/2503.16338) | [:computer: Code](https://github.com/shengjun-zhang/GGN)｜[:globe_with_meridians: Project Page](https://shengjun-zhang.github.io/GGN/)]
- PixelGaussian: Generalizable 3D Gaussian Reconstruction from Arbitrary Views. [[:page_facing_up: Paper](https://arxiv.org/abs/2410.18979) | [:computer: Code](https://github.com/Barrybarry-Smith/PixelGaussian)｜[:globe_with_meridians: Project Page](https://wzzheng.net/PixelGaussian)]
- FreeSplat++: Generalizable 3D Gaussian Splatting for Efficient Indoor Scene Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2503.22986) | [:computer: Code](https://github.com/wangys16/FreeSplatPP)｜[:globe_with_meridians: Project Page](https://wangys16.github.io/FreeSplatPP-Page/)]
- LongSplat: Online Generalizable 3D Gaussian Splatting from Long Sequence Images. [[:page_facing_up: Paper](https://arxiv.org/abs/2507.16144) | [:computer: Code](https://github.com/NVlabs/LongSplat)｜[:globe_with_meridians: Project Page](https://linjohnss.github.io/longsplat)]

## Data & Visual Augmentation

### Data Augmentation

- MegaSynth: Scaling Up 3D Scene Reconstruction with Synthesized Data. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.14166) | [:computer: Code](https://github.com/hwjiang1510/MegaSynth)｜[:globe_with_meridians: Project Page](https://hwjiang1510.github.io/MegaSynth/)]
- Puzzles: Unbounded Video-Depth Augmentation for Scalable End-to-End 3D Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.23863) | [:computer: Code](https://github.com/Jiahao-Ma/puzzles-code)｜[:globe_with_meridians: Project Page](https://jiahao-ma.github.io/puzzles/)]
- Aug3D: Augmenting Large Scale Outdoor Datasets for Generalizable Novel View Synthesis. [[:page_facing_up: Paper](https://arxiv.org/abs/2501.06431)]
- MVBoost: Boost 3D Reconstruction with Multi-View Refinement.

### Visual Augmentation

- MVSplat360: Feed-Forward 360 Scene Synthesis from Sparse Views. [[:page_facing_up: Paper](https://arxiv.org/abs/2411.04924) | [:computer: Code](https://github.com/donydchen/mvsplat360)｜[:globe_with_meridians: Project Page](https://donydchen.github.io/mvsplat360)]
- latentSplat: Autoencoding Variational Gaussians for Fast Generalizable 3D Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2403.16292) | [:computer: Code](https://github.com/Chrixtar/latentsplat)｜[:globe_with_meridians: Project Page](https://geometric-rl.mpi-inf.mpg.de/latentsplat/)]
- ProSplat: Improved Feed-Forward 3D Gaussian Splatting for Wide-Baseline Sparse Views. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.07670)]
- Difix3D+: Improving 3D Reconstructions with Single-Step Diffusion Models.
- Reconstruct, Inpaint, Finetune: Dynamic Novel-view Synthesis from Monocular Videos. [[:page_facing_up: Paper](https://arxiv.org/abs/2507.12646)]

## Temporal-aware Models

### Online Streaming

- StreamSplat: Towards Online Dynamic 3D Reconstruction from Uncalibrated Video Streams. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.08862) | [:computer: Code](https://github.com/DSL-Lab/StreamSpat)]
- Continuous 3D Perception Model with Persistent State. [[:page_facing_up: Paper](https://arxiv.org/abs/2501.12387) | [:computer: Code](https://github.com/CUT3R/CUT3R)｜[:globe_with_meridians: Project Page](https://cut3r.github.io/)]
- DGS-LRM: Real-Time Deformable 3D Gaussian Reconstruction From Monocular Videos. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.09997) ｜[:globe_with_meridians: Project Page](https://hubert0527.github.io/dgslrm/)]
- Stream3R: Scalable Sequential 3D Reconstruction with Causal Transformer. [[:page_facing_up: Paper](https://arxiv.org/abs/2508.10893)]
- LongStream: Long-Sequence Streaming Autoregressive Visual Geometry. [[:page_facing_up: Paper](https://arxiv.org/abs/2602.13172)]

### Offline Processing

- L4GM: Large 4D Gaussian Reconstruction Model.
- 4D-LRM: Large Space-Time Reconstruction Model From and To Any View at Any Time. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.18890)]
- MonST3R: A Simple Approach for Estimating Geometry in the Presence of Motion. [[:page_facing_up: Paper](https://monst3r-project.github.io/files/monst3r_paper.pdf) | [:computer: Code](https://github.com/Junyi42/monst3r)｜[:globe_with_meridians: Project Page](https://monst3r-project.github.io/)]
- Easi3R: Estimating Disentangled Motion from DUSt3R Without Training. [[:page_facing_up: Paper](https://arxiv.org/abs/2503.24391) | [:computer: Code](https://github.com/Inception3D/Easi3R)｜[:globe_with_meridians: Project Page](https://easi3r.github.io/)]
- 4DGT: Learning a 4D Gaussian Transformer Using Real-World Monocular Videos. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.08015) | [:computer: Code](https://github.com/facebookresearch/4dgt)｜[:globe_with_meridians: Project Page](https://4dgt.github.io/)]
- MoVieS: Motion-Aware 4D Dynamic View Synthesis in One Second. [[:page_facing_up: Paper](https://arxiv.org/abs/2507.10065) | [:computer: Code](https://github.com/chenguolin/MoVieS)｜[:globe_with_meridians: Project Page](https://chenguolin.github.io/projects/MoVieS/)]
- 4Real-Video-V2: Fused View-Time Attention and Feedforward Reconstruction for 4D Scene Generation. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.18839) ｜[:globe_with_meridians: Project Page](https://snap-research.github.io/4Real-Video-V2/)]
- MonoFusion: Sparse-View 4D Reconstruction via Monocular Fusion. [[:page_facing_up: Paper](https://arxiv.org/abs/2507.23782) | [:computer: Code](https://github.com/ImNotPrepared/MonoFusion)｜[:globe_with_meridians: Project Page](https://imnotprepared.github.io/research/25_DSR/)]
- Self-Supervised Monocular 4D Scene Reconstruction for Egocentric Videos. [[:page_facing_up: Paper](https://arxiv.org/abs/2411.09145)]
- Feed-forward Bullet-Time Reconstruction of Dynamic Scenes from Monocular Videos. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.03526)]

### Interactive Modeling

- PIXIE: Physics from Pixels for Interactive Feed-Forward Scene Modeling. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.05361)]
- PhysGM: Physical Gaussian Modeling for Interactive 3D Scene Editing. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.10442)]

### Specialized Tasks

- DAS3R: Dynamics-Aware Gaussian Splatting for Static Scene Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.19584) | [:computer: Code](https://github.com/kai422/DAS3R)｜[:globe_with_meridians: Project Page](https://kai422.github.io/DAS3R/)]
- St4RTrack: Simultaneous 4D Reconstruction and Tracking in the World.

## Datasets and Benchmarks

| <img width="100%" src="https://ff3d-survey.github.io/assets/dataset.png"> |
|:-:|

## Geometry Oriented

- DTU: Large Scale Multi-view Stereopsis Evaluation. [[:page_facing_up: Paper](https://ieeexplore.ieee.org/document/6909453) | [:globe_with_meridians: Project Page](http://roboimagedata.compute.dtu.dk/?page_id=36)]
- 7Scenes: Scene Coordinate Regression Forests for Camera Relocalization in RGB-D Images. [[:page_facing_up: Paper](https://ieeexplore.ieee.org/document/6619221) | [:globe_with_meridians: Project Page](https://www.microsoft.com/en-us/research/project/rgb-d-dataset-7-scenes/)]

## Visual Oriented

- NeRF-Synthetic: NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis. [[:page_facing_up: Paper](https://arxiv.org/abs/2003.08934) | [:computer: Code](https://github.com/bmild/nerf)｜[:globe_with_meridians: Project Page](http://matthewtancik.com/nerf) | [🔗Data Link](https://drive.google.com/drive/folders/1cK3UDIJqKAAm7zyrxRYVFJ0BRMgrwhh4)]
- Neural 3D Mesh Renderer (NMR): Neural 3D Mesh Renderer. [[:page_facing_up: Paper](https://arxiv.org/abs/1711.07566) | [:computer: Code](https://github.com/daniilidis-group/neural_renderer)]
- CelebA: Deep Learning Face Attributes in the Wild. [[:page_facing_up: Paper](https://arxiv.org/abs/1411.7766) | [:globe_with_meridians: Project Page](https://liuziwei7.github.io/projects/FaceAttributes.html) | [🔗Data Link](https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)]
- Consistent4D: Consistent 360° Dynamic Object Generation from Monocular Video. [[:page_facing_up: Paper](https://arxiv.org/abs/2311.02848) | [:computer: Code](https://github.com/yanqinJiang/Consistent4D?tab=readme-ov-file)｜[:globe_with_meridians: Project Page](https://consistent4d.github.io/) | [🔗Data Link](https://drive.google.com/file/d/1mJNhFKvzZ-8icAw6KC-W-sf7JmmmMUkx/view?usp=sharing)]
- NYUv2: Indoor Segmentation and Support Inference from RGBD Images. [[:page_facing_up: Paper](https://link.springer.com/chapter/10.1007/978-3-642-33715-4_54) | [:globe_with_meridians: Project Page](https://cs.nyu.edu/~fergus/datasets/nyu_depth_v2.html) | [🔗Data Link](https://cs.nyu.edu/~fergus/datasets/nyu_depth_v2.html#raw_parts)]
- Habitat: A Platform for Embodied AI Research. [[:page_facing_up: Paper](https://arxiv.org/abs/1904.01201) | [:computer: Code](https://github.com/facebookresearch/habitat-lab) | [🔗Data Link](https://github.com/facebookresearch/habitat-lab/blob/main/DATASETS.md)]
- Hot3D: Hand and Object Tracking in 3D from Egocentric Multi-view Videos. [[:page_facing_up: Paper](https://arxiv.org/abs/2406.09598) | [:computer: Code](https://github.com/facebookresearch/hot3d)｜[:globe_with_meridians: Project Page](https://facebookresearch.github.io/hot3d/) | [🔗Data Link](https://www.projectaria.com/datasets/hot3D/)]
- ACID: Infinite Nature: Perpetual View Generation of Natural Scenes from a Single Image. [[:page_facing_up: Paper](https://arxiv.org/abs/2012.09855) ｜[:globe_with_meridians: Project Page](https://www.acidb.net/dataset) | [🔗Data Link](https://www.acidb.net/download)]
- ENeRF-Outdoor: Efficient Neural Radiance Fields for Interactive Free-viewpoint Video. [[:page_facing_up: Paper](https://arxiv.org/abs/2112.01517) | [:computer: Code](https://github.com/zju3dv/ENeRF)｜[:globe_with_meridians: Project Page](https://zju3dv.github.io/enerf/) | [🔗Data Link](https://github.com/zju3dv/ENeRF/blob/master/docs/enerf_outdoor.md)]
- LLFF: Local Light Field Fusion: Practical View Synthesis with Prescriptive Sampling Guidelines. [[:page_facing_up: Paper](https://arxiv.org/abs/1905.00889) | [:computer: Code](https://github.com/Fyusion/LLFF)｜[:globe_with_meridians: Project Page](https://bmild.github.io/llff/) | [🔗Data Link](https://bmild.github.io/llff/)]
- Neural3DV: Neural 3D Video Synthesis from Multi-view Video. [[:page_facing_up: Paper](https://arxiv.org/abs/2103.02597) | [:computer: Code](https://github.com/facebookresearch/Neural_3D_Video)｜[:globe_with_meridians: Project Page](https://neural-3d-video.github.io/) | [🔗Data Link](https://github.com/facebookresearch/Neural_3D_Video)]
- EgoExo4D: Understanding Skilled Human Activity from First- and Third-Person Perspectives. [[:page_facing_up: Paper](https://arxiv.org/abs/2311.18259) | [:computer: Code](https://github.com/EGO4D)｜[:globe_with_meridians: Project Page](https://ego-exo4d-data.org/) | [🔗Data Link](https://ego4ddataset.com/egoexo-license/)]
- DAVIS: A Benchmark Dataset and Evaluation Methodology for Video Object Segmentation. [[:page_facing_up: Paper](https://arxiv.org/abs/1704.00675) | [:computer: Code](https://github.com/fperazzi/davis-2017)｜[:globe_with_meridians: Project Page](https://davischallenge.org/davis2017) | [🔗Data Link](https://davischallenge.org/davis2017/code.html)]
- Youtube-VOS: Sequence-to-sequence Video Object Segmentation. [[:page_facing_up: Paper](https://arxiv.org/abs/1809.03327) ｜[:globe_with_meridians: Project Page](https://youtube-vos.org/) | [🔗Data Link](https://youtube-vos.org/dataset/)]
- DL3DV-10K: A Large-Scale Scene Dataset for Deep Learning-based 3D Vision. [[:page_facing_up: Paper](https://arxiv.org/abs/2312.16256) | [:computer: Code](https://github.com/DL3DV-10K/Dataset)｜[:globe_with_meridians: Project Page](https://dl3dv-10k.github.io/DL3DV-10K/) | [🔗Data Link](https://huggingface.co/DL3DV/datasets)]
- RealEstate10K: Stereo Magnification: Learning View Synthesis Using Multiplane Images. [[:page_facing_up: Paper](https://research.google/pubs/pub46965/) ｜[:globe_with_meridians: Project Page](https://google.github.io/realestate10k/) | [🔗Data Link](https://google.github.io/realestate10k/download.html)]

## Mixed

- Google Scanned Objects (GSO): A High-Quality Dataset of 3D Scanned Household Items. [[:page_facing_up: Paper](https://arxiv.org/abs/2204.11918) | [:globe_with_meridians: Project Page](https://research.google/blog/scanned-objects-by-google-research-a-dataset-of-3d-scanned-common-household-items/) | [🔗Data Link](https://app.gazebosim.org/GoogleResearch/fuel/collections/Scanned%20Objects%20by%20Google%20Research)]
- OmniObject3D: Large-Vocabulary 3D Object Dataset for Realistic Perception, Reconstruction and Generation. [[:page_facing_up: Paper](https://arxiv.org/abs/2301.07525) | [:computer: Code](https://github.com/omniobject3d/OmniObject3D/tree/main)｜[:globe_with_meridians: Project Page](https://omniobject3d.github.io/) | [🔗Data Link](https://openxlab.org.cn/datasets/OpenXDLab/OmniObject3D-New/explore/main)]
- CO3D: Common Objects in 3D: Large-Scale Learning and Evaluation of Real-Life 3D Category Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2109.00512) | [:computer: Code](https://github.com/facebookresearch/co3d)｜[:globe_with_meridians: Project Page](https://eval.ai/web/challenges/challenge-page/1819/overview) | [🔗Data Link](https://github.com/facebookresearch/co3d/blob/main/co3d/dataset/download_dataset_impl.py)]
- WildRGBD: RGBD Objects in the Wild: Scaling Real-World 3D Object Learning from RGB-D Videos. [[:page_facing_up: Paper](https://arxiv.org/abs/2401.12592) | [:computer: Code](https://github.com/wildrgbd/wildrgbd)｜[:globe_with_meridians: Project Page](https://wildrgbd.github.io/) | [🔗Data Link](https://github.com/wildrgbd/wildrgbd/blob/main/download.py)]
- ShapeNet: An Information-Rich 3D Model Repository. [[:page_facing_up: Paper](https://arxiv.org/abs/1512.03012) ｜[:globe_with_meridians: Project Page](https://shapenet.org/) | [🔗Data Link](https://shapenet.org/login/)]
- MVImgNet: A Large-Scale Dataset of Multi-View Images. [[:page_facing_up: Paper](https://arxiv.org/abs/2303.06042) | [:computer: Code](https://github.com/GAP-LAB-CUHK-SZ/MVImgNet) | [🔗Data Link](https://github.com/GAP-LAB-CUHK-SZ/MVImgNet/blob/main/download_tool.zip)]
- Objaverse: A Universe of Annotated 3D Objects. [[:page_facing_up: Paper](https://arxiv.org/abs/2307.05663) | [:computer: Code](https://github.com/allenai/objaverse-xl)｜[:globe_with_meridians: Project Page](https://objaverse.allenai.org/) | [🔗Data Link](https://huggingface.co/datasets/allenai/objaverse-xl)]
- Objaverse-XL: A Universe of 10M+ 3D Objects. [[:page_facing_up: Paper](https://arxiv.org/abs/2307.05663) | [:computer: Code](https://github.com/allenai/objaverse-xl)｜[:globe_with_meridians: Project Page](https://objaverse.allenai.org/) | [🔗Data Link](https://huggingface.co/datasets/allenai/objaverse-xl)]
- DeepVoxels: Learning Persistent 3D Feature Embeddings. [[:page_facing_up: Paper](https://arxiv.org/abs/1812.01024) | [:computer: Code](https://github.com/vsitzmann/deepvoxels)｜[:globe_with_meridians: Project Page](https://www.vincentsitzmann.com/deepvoxels/) | [🔗Data Link](https://drive.google.com/open?id=1ScsRlnzy9Bd_n-xw83SP-0t548v63mPH)]
- MultiShapeNet: Scene Representation Transformer: Geometry-Free Novel View Synthesis Through Set-Latent Scene Representations. [[:page_facing_up: Paper](https://arxiv.org/abs/2111.13152) | [:computer: Code](https://srt-paper.github.io/#code)｜[:globe_with_meridians: Project Page](https://srt-paper.github.io/) | [🔗Data Link](https://srt-paper.github.io/#dataset)]
- Amazon Berkeley Objects (ABO): Dataset and Benchmarks for Real-World 3D Object Understanding. [[:page_facing_up: Paper](https://amazon-berkeley-objects.s3.amazonaws.com/static_html/ABO_CVPR2022.pdf) ｜[:globe_with_meridians: Project Page](https://amazon-berkeley-objects.s3.amazonaws.com/index.html) | [🔗Data Link](https://amazon-berkeley-objects.s3.amazonaws.com/index.html#download)]
- Replica: A Digital Replica of Indoor Spaces. [[:page_facing_up: Paper](https://arxiv.org/abs/1906.05797) | [:computer: Code](https://github.com/facebookresearch/Replica-Dataset) | [🔗Data Link](https://github.com/facebookresearch/Replica-Dataset/blob/main/download.sh)]
- TUM RGBD: Evaluating Egomotion and Structure-from-Motion Approaches Using the TUM RGB-D Benchmark. [[:page_facing_up: Paper](https://www.semanticscholar.org/paper/Evaluating-Egomotion-and-Structure-from-Motion-the-Sturm-Burgard/3ad29f46efa040eb14d15be48a563af5b75463a8) ｜[:globe_with_meridians: Project Page](https://cvg.cit.tum.de/data/datasets/rgbd-dataset) | [🔗Data Link](http://vision.in.tum.de/data/datasets/rgbd-dataset/download)]
- Matterport3D: Learning from RGB-D Data in Indoor Environments. [[:page_facing_up: Paper](https://arxiv.org/pdf/1709.06158.pdf) | [:computer: Code](https://github.com/niessner/Matterport)｜[:globe_with_meridians: Project Page](https://niessner.github.io/Matterport/) | [🔗Data Link](https://niessner.github.io/Matterport/#download)]
- Hypersim: A Photorealistic Synthetic Dataset for Holistic Indoor Scene Understanding. [[:page_facing_up: Paper](https://arxiv.org/abs/2011.02523) | [:computer: Code](https://github.com/apple/ml-hypersim) | [🔗Data Link](https://github.com/apple/ml-hypersim/blob/main/code/python/tools/dataset_download_images.py)]
- ScanNet: Richly-annotated 3D Reconstructions of Indoor Scenes. [[:page_facing_up: Paper](https://arxiv.org/abs/1702.04405) | [:computer: Code](https://github.com/ScanNet/ScanNet)｜[:globe_with_meridians: Project Page](http://www.scan-net.org/) | [🔗Data Link](https://github.com/ScanNet/ScanNet?tab=readme-ov-file#scannet-data)]
- ScanNet++: A High-Fidelity Dataset of 3D Indoor Scenes. [[:page_facing_up: Paper](https://arxiv.org/abs/2308.11417) | [:computer: Code](https://github.com/scannetpp/scannetpp)｜[:globe_with_meridians: Project Page](https://scannetpp.mlsg.cit.tum.de/scannetpp/) | [🔗Data Link](https://scannetpp.mlsg.cit.tum.de/scannetpp/register)]
- ARKitScenes: A Diverse Real-World Dataset for 3D Indoor Scene Understanding Using Mobile RGB-D Data. [[:page_facing_up: Paper](https://openreview.net/forum?id=tjZjv_qh_CE) | [:computer: Code](https://github.com/apple/ARKitScenes) | [🔗Data Link](https://github.com/apple/ARKitScenes/blob/main/DATA.md)]
- Virtual KITTI 2. [[:page_facing_up: Paper](https://arxiv.org/abs/2001.10773) ｜[:globe_with_meridians: Project Page](https://europe.naverlabs.com/research/proxy-virtual-worlds/) | [🔗Data Link](https://download.europe.naverlabs.com//virtual_kitti_2.0.3/vkitti_2.0.3_md5_checksums.txt)]
- Spring: A High-Resolution High-Detail Dataset and Benchmark for Scene Flow, Optical Flow and Stereo. [[:page_facing_up: Paper](https://arxiv.org/abs/2303.01943) | [:computer: Code](https://github.com/cv-stuttgart/sceneflow_from_blender)｜[:globe_with_meridians: Project Page](https://spring-benchmark.org/) | [🔗Data Link](https://spring-benchmark.org/download)]
- MegaDepth: Learning Single-View Depth Prediction from Internet Photos. [[:page_facing_up: Paper](https://www.cs.cornell.edu/projects/megadepth/paper.pdf) | [:computer: Code](https://github.com/lixx2938/MegaDepth)｜[:globe_with_meridians: Project Page](https://www.cs.cornell.edu/projects/megadepth/) | [🔗Data Link](https://www.cs.cornell.edu/projects/megadepth/dataset/Megadepth_v1/MegaDepth_v1.tar.gz)]
- PointOdyssey: A Large-Scale Synthetic Dataset for Long-Term Point Tracking. [[:page_facing_up: Paper](https://arxiv.org/abs/2307.15055) | [:computer: Code](https://github.com/aharley/pips2)｜[:globe_with_meridians: Project Page](https://pointodyssey.com/) | [🔗Data Link](https://drive.google.com/drive/folders/1W6wxsbKbTdtV8-2TwToqa_QgLqRY3ft0?usp=drive_link)]
- TartanAir: A Dataset to Push the Limits of Visual SLAM. [[:page_facing_up: Paper](https://arxiv.org/abs/2003.14338) ｜[:globe_with_meridians: Project Page](https://theairlab.org/tartanair-dataset/) | [🔗Data Link](https://github.com/castacks/tartanair_tools)]
- Waymo: Scalability in Perception for Autonomous Driving. [[:page_facing_up: Paper](https://arxiv.org/abs/1912.04838) | [:computer: Code](https://github.com/waymo-research/waymo-open-dataset)｜[:globe_with_meridians: Project Page](https://waymo.com/open/) | [🔗Data Link](https://waymo.com/open/licensing/?continue=%2Fopen%2Fdownload%2F)]
- nuScenes: A Multimodal Dataset for Autonomous Driving. [[:page_facing_up: Paper](https://arxiv.org/abs/1903.11027) | [:globe_with_meridians: Project Page](https://www.nuscenes.org/) | [🔗Data Link](https://www.nuscenes.org/nuscenes#download)]
- Mip-NeRF 360: Unbounded Anti-Aliased Neural Radiance Fields. [[:page_facing_up: Paper](https://arxiv.org/abs/2111.12077) | [:computer: Code](https://github.com/google-research/multinerf)｜[:globe_with_meridians: Project Page](https://jonbarron.info/mipnerf360/) | [🔗Data Link](http://storage.googleapis.com/gresearch/refraw360/360_v2.zip)]
- Tanks and Temples: Benchmarking Large-Scale Scene Reconstruction. [[:page_facing_up: Paper](https://dl.acm.org/doi/10.1145/3072959.3073599) | [:globe_with_meridians: Project Page](https://www.tanksandtemples.org/)]
- ETH3D: A Multi-View Stereo Benchmark with High-Resolution Images and Multi-Camera Videos. [[:page_facing_up: Paper](https://www.eth3d.net/data/schoeps2017cvpr.pdf) | [:computer: Code](https://github.com/ETH3D)｜[:globe_with_meridians: Project Page](https://www.eth3d.net/) | [🔗Data Link](https://www.eth3d.net/slam_datasets)]
- BlendedMVS: A Large-Scale Dataset for Generalized Multi-View Stereo Networks. [[:page_facing_up: Paper](https://arxiv.org/abs/1911.10127) | [:computer: Code](https://github.com/YoYo000/BlendedMVS) | [🔗Data Link](https://github.com/YoYo000/BlendedMVS/releases/download/v1.0.0/BlendedMVS.zip)]
- DyCheck: Dynamic Gaussian Marbles for Novel View Synthesis of Casual Monocular Videos. [[:page_facing_up: Paper](https://arxiv.org/abs/2406.18717) | [:computer: Code](https://github.com/coltonstearns/dynamic-gaussian-marbles)｜[:globe_with_meridians: Project Page](https://geometry.stanford.edu/projects/dynamic-gaussian-marbles.github.io/) | [🔗Data Link](https://drive.google.com/drive/folders/1hKlpqofQt4PhKLWw7kb4tI5CFgJE4Iu-?usp=drive_link)]

## Applications

| <img width="100%" src="https://ff3d-survey.github.io/assets/application.png"> |
|:-:|

## Autonomous Driving

- Driv3R: Learning Dense 4D Reconstruction for Autonomous Driving. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.06777) | [:computer: Code](https://github.com/Barrybarry-Smith/Driv3R)｜[:globe_with_meridians: Project Page](https://wzzheng.net/Driv3R/)]
- InfiniCube: Unbounded and Controllable Dynamic 3D Driving Scene Generation with World-Guided Video Models. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.03934) | [:computer: Code](https://github.com/nv-tlabs/InfiniCube)｜[:globe_with_meridians: Project Page](https://research.nvidia.com/labs/toronto-ai/infinicube/)]
- DrivingRecon: Large 4D Gaussian Reconstruction Model for Autonomous Driving. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.09043) | [:computer: Code](https://github.com/EnVision-Research/DriveRecon)]
- GEN3C: 3D-Informed World-Consistent Video Generation with Precise Camera Control. [[:page_facing_up: Paper](https://arxiv.org/abs/2503.03751) | [:computer: Code](https://github.com/nv-tlabs/GEN3C)｜[:globe_with_meridians: Project Page](https://research.nvidia.com/labs/toronto-ai/GEN3C/)]
- DrivingForward: Feed-forward 3D Gaussian Splatting for Driving Scene Reconstruction from Flexible Surround-view Input. [[:page_facing_up: Paper](https://arxiv.org/abs/2409.12753) | [:computer: Code](https://github.com/fangzhou2000/DrivingForward)]
- STORM: Spatio-Temporal Reconstruction Model for Large-Scale Outdoor Scenes. [[:page_facing_up: Paper](https://arxiv.org/abs/2501.00602) | [:computer: Code](https://github.com/NVlabs/GaussianSTORM)｜[:globe_with_meridians: Project Page](https://jiawei-yang.github.io/STORM/)]
- SCube: Instant Large-Scale Scene Reconstruction using VoxSplats. [[:page_facing_up: Paper](https://arxiv.org/abs/2410.20030) | [:computer: Code](https://github.com/nv-tlabs/SCube)｜[:globe_with_meridians: Project Page](https://research.nvidia.com/labs/toronto-ai/scube/)]
- EVolSplat: Efficient Volume-based Gaussian Splatting for Urban View Synthesis. [[:page_facing_up: Paper](https://arxiv.org/abs/2503.20168) | [:computer: Code](https://github.com/Miaosheng1/EVolSplat)｜[:globe_with_meridians: Project Page](https://xdimlab.github.io/EVolSplat/)]
- Omni-Scene: Omni-Gaussian Representation for Ego-Centric Sparse-View Scene Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.06273) | [:computer: Code](https://github.com/WU-CVGL/OmniScene)｜[:globe_with_meridians: Project Page](https://wswdx.github.io/omniscene/)]
- BEV-GS: Feed-forward Gaussian Splatting in Bird's-Eye-View for Road Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2504.13207) | [:computer: Code](https://github.com/cat-wwh/BEV-GS)]
- Efficient Depth-guided Urban View Synthesis. [[:page_facing_up: Paper](https://arxiv.org/abs/2407.12395) | [:computer: Code](https://github.com/Miaosheng1/EDUS)｜[:globe_with_meridians: Project Page](https://xdimlab.github.io/EDUS/)]
- DriveGen3D: Boosting Feed-Forward Driving Scene Generation with Efficient Video Diffusion. [[:page_facing_up: Paper](https://arxiv.org/abs/2510.15264)｜[:globe_with_meridians: Project Page](https://lhmd.top/drivegen3d)]
- WorldSplat: Gaussian-Centric Feed-Forward 4D Scene Generation for Autonomous Driving. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.23402) | [:computer: Code](https://github.com/wm-research/worldsplat)｜[:globe_with_meridians: Project Page](https://wm-research.github.io/worldsplat/)]

## Robotics

### Manipulation

- GraspNeRF: Multiview-based 6-DoF Grasp Detection for Transparent and Specular Objects Using Generalizable NeRF. [[:page_facing_up: Paper](https://arxiv.org/abs/2210.06575) | [:computer: Code](https://github.com/PKU-EPIC/GraspNeRF)｜[:globe_with_meridians: Project Page](https://pku-epic.github.io/GraspNeRF/)]
- ManiGaussian: Dynamic Gaussian Splatting for Multi-task Robotic Manipulation. [[:page_facing_up: Paper](https://arxiv.org/abs/2403.08321) | [:computer: Code](https://github.com/GuanxingLu/ManiGaussian)｜[:globe_with_meridians: Project Page](https://guanxinglu.github.io/ManiGaussian/)]
- ManiGaussian++: General Robotic Bimanual Manipulation with Hierarchical Gaussian World Model. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.19842) | [:computer: Code](https://github.com/April-Yz/ManiGaussian_Bimanual)]
- Query-based Semantic Gaussian Field for Scene Representation in Reinforcement Learning. [[:page_facing_up: Paper](https://arxiv.org/abs/2406.02370)]
- GAF: Gaussian Action Field as a Dynamic World Model for Robotic Manipulation. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.14135)｜[:globe_with_meridians: Project Page](https://chaiying1.github.io/GAF.github.io/project_page/)]
- GaussianGrasper: 3D Language Gaussian Splatting for Open-Vocabulary Robotic Grasping. [[:page_facing_up: Paper](https://arxiv.org/abs/2403.09637) | [:computer: Code](https://github.com/MrSecant/GaussianGrasper)]
- EmbodiedSplat: Personalized Real-to-Sim-to-Real Navigation with Gaussian Splats from a Mobile Device. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.17430)｜[:globe_with_meridians: Project Page](https://gchhablani.github.io/embodied-splat/)]

### Navigation

- IGL-Nav: Incremental 3D Gaussian Localization for Image-goal Navigation. [[:page_facing_up: Paper](https://arxiv.org/abs/2508.00823) | [:computer: Code](https://github.com/GWxuan/IGL-Nav)｜[:globe_with_meridians: Project Page](https://gwxuan.github.io/IGL-Nav/)]
- VR-Robo: A Real-to-Sim-to-Real Framework for Visual Robot Navigation and Locomotion. [[:page_facing_up: Paper](https://arxiv.org/abs/2502.01536) | [:computer: Code](https://github.com/zst1406217/VR-Robo)｜[:globe_with_meridians: Project Page](https://vr-robo.github.io/)]
- GS-LTS: 3D Gaussian Splatting-Based Adaptive Modeling for Long-Term Service Robots. [[:page_facing_up: Paper](https://arxiv.org/abs/2503.17733)｜[:globe_with_meridians: Project Page](https://vipl-vsu.github.io/3DGS-LTS)]
- UnitedVLN: Generalizable Gaussian Splatting for Continuous Vision-Language Navigation. [[:page_facing_up: Paper](https://arxiv.org/abs/2411.16053)]

## SfM & SLAM

### SFM

- Visual Geometry Grounded Deep Structure From Motion. [[:page_facing_up: Paper](https://arxiv.org/abs/2312.04563) | [:computer: Code](https://github.com/facebookresearch/vggsfm)｜[:globe_with_meridians: Project Page](https://vggsfm.github.io/)]
- Light3R-SfM: Towards Feed-forward Structure-from-Motion. [[:page_facing_up: Paper](https://arxiv.org/abs/2501.14914)｜[:globe_with_meridians: Project Page](https://selflein.github.io/Light3R/)]
- Mast3r-sfm: A Fully-Integrated Solution for Unconstrained Structure-from-Motion. [[:page_facing_up: Paper](https://arxiv.org/abs/2409.19152) | [:computer: Code](https://github.com/naver/mast3r)]
- Regist3R: Incremental Registration with Stereo Foundation Model. [[:page_facing_up: Paper](https://arxiv.org/abs/2504.12356) | [:computer: Code](https://github.com/Liu-SD/Regist3R)]
- VGGT-Long: Chunk it, Loop it, Align it -- Pushing VGGT's Limits on Kilometer-scale Long RGB Sequences. [[:page_facing_up: Paper](https://arxiv.org/abs/2507.16443) | [:computer: Code](https://github.com/DengKaiCQ/VGGT-Long)]
- Fast3R: Towards 3D Reconstruction of 1000+ Images in One Forward Pass. [[:page_facing_up: Paper](https://arxiv.org/abs/2501.13928) | [:computer: Code](https://github.com/facebookresearch/fast3r)｜[:globe_with_meridians: Project Page](https://fast3r-3d.github.io/)]
- FLARE: Feed-forward Geometry, Appearance and Camera Estimation from Uncalibrated Sparse Views. [[:page_facing_up: Paper](https://arxiv.org/abs/2502.12138) | [:computer: Code](https://github.com/ant-research/FLARE)｜[:globe_with_meridians: Project Page](https://zhanghe3z.github.io/FLARE/)]

### SLAM

- MASt3R-SLAM: Real-Time Dense SLAM with 3D Reconstruction Priors. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.12392) | [:computer: Code](https://github.com/rmurai0610/MASt3R-SLAM)｜[:globe_with_meridians: Project Page](https://edexheim.github.io/mast3r-slam/)]
- SLAM3R. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.09401) | [:computer: Code](https://github.com/PKU-VCL-3DV/SLAM3R)]
- VGGT-SLAM. [[:page_facing_up: Paper](https://arxiv.org/abs/2505.12549) | [:computer: Code](https://github.com/MIT-SPARK/VGGT-SLAM)]
- ARTDECO: Towards Efficient and High-Fidelity On-the-Fly 3D Reconstruction with Structured Scene Representation. [[:page_facing_up: Paper](https://arxiv.org/abs/2510.08551)]
- EC3R-SLAM: Efficient and Consistent Monocular Dense SLAM with Feed-Forward 3D Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2510.02080)]
- MASt3R-Fusion: Integrating Feed-Forward Visual Model with IMU, GNSS for High-Functionality SLAM. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.20757)]
- ViSTA-SLAM: Visual SLAM with Symmetric Two-view Association. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.01584) | [:computer: Code](https://github.com/zhangganlin/vista-slam)｜[:globe_with_meridians: Project Page](https://ganlinzhang.xyz/vista-slam/)]

## Scene Understanding

### Semantic

- SLGaussian: Fast Language Gaussian Splatting in Sparse Views. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.08331)]
- GSemSplat: Generalizable Semantic 3D Gaussian Splatting from Uncalibrated Image Pairs. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.16932)]
- SegMASt3R: Geometry Grounded Segment Matching. [[:page_facing_up: Paper](https://arxiv.org/abs/2510.05051)｜[:globe_with_meridians: Project Page](https://segmast3r.github.io/)]
- PartField: Learning 3D Feature Fields for Part Segmentation and Beyond. [[:page_facing_up: Paper](https://arxiv.org/abs/2504.11451) | [:computer: Code](https://github.com/nv-tlabs/PartField)｜[:globe_with_meridians: Project Page](https://research.nvidia.com/labs/toronto-ai/partfield-release/)]
- Semantic Gaussians: Open-Vocabulary Scene Understanding with 3D Gaussian Splatting. [[:page_facing_up: Paper](https://arxiv.org/abs/2403.15624) | [:computer: Code](https://github.com/sharinka0715/semantic-gaussians)｜[:globe_with_meridians: Project Page](https://sharinka0715.github.io/semantic-gaussians/)]
- SemanticSplat: Feed-Forward 3D Scene Understanding with Language-Aware Gaussian Fields. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.09565) | [:computer: Code](https://semanticsplat.github.io/)｜[:globe_with_meridians: Project Page](https://semanticsplat.github.io/)]
- UniForward: Unified 3D Scene and Semantic Field Reconstruction via Feed-Forward Gaussian Splatting from Only Sparse-View Images. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.09378)]
- Large Spatial Model: End-to-end Unposed Images to Semantic 3D. [[:page_facing_up: Paper](https://arxiv.org/abs/2410.18956) | [:computer: Code](https://github.com/NVlabs/LSM)｜[:globe_with_meridians: Project Page](https://largespatialmodel.github.io/)]
- AlignGS: Aligning Geometry and Semantics for Robust Indoor Reconstruction from Sparse Views. [[:page_facing_up: Paper](https://arxiv.org/abs/2510.07839)｜[:globe_with_meridians: Project Page](https://mediax-sjtu.github.io/AlignGS/)]

### 3D Scene Understanding

- MLLMs Need 3D-Aware Representation Supervision for Scene Understanding. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.01946) | [:computer: Code](https://github.com/Visual-AI/3DRS)｜[:globe_with_meridians: Project Page](https://visual-ai.github.io/3drs)]
- Spatio-Temporal LLM: Reasoning about Environments and Actions. [[:page_facing_up: Paper](https://arxiv.org/abs/2507.05258) | [:computer: Code](https://github.com/zoezheng126/Spatio-Temporal-LLM)｜[:globe_with_meridians: Project Page](https://zoezheng126.github.io/STLLM-website/)]
- Spatial-MLLM: Boosting MLLM Capabilities in Visual-based Spatial Intelligence. [[:page_facing_up: Paper](https://arxiv.org/abs/2505.23747) | [:computer: Code](https://github.com/diankun-wu/Spatial-MLLM)｜[:globe_with_meridians: Project Page](https://diankun-wu.github.io/Spatial-MLLM/)]
- Learning from Videos for 3D World: Enhancing MLLMs with 3D Vision Geometry Priors. [[:page_facing_up: Paper](https://arxiv.org/abs/2505.24625) | [:computer: Code](https://github.com/LaVi-Lab/VG-LLM)｜[:globe_with_meridians: Project Page](https://lavi-lab.github.io/VG-LLM/)]
- VLM-3R: Vision-Language Models Augmented with Instruction-Aligned 3D Reconstruction. [[:page_facing_up: Paper](https://arxiv.org/abs/2505.20279) | [:computer: Code](https://github.com/VITA-Group/VLM-3R)｜[:globe_with_meridians: Project Page](https://vlm-3r.github.io/)]

## Video Generation

### Reconstruction-enhanced Video Generation

- MVSplat360: Feed-Forward 360 Scene Synthesis from Sparse Views. [[:page_facing_up: Paper](https://arxiv.org/abs/2411.04924) | [:computer: Code](https://github.com/donydchen/mvsplat360)｜[:globe_with_meridians: Project Page](https://donydchen.github.io/mvsplat360/)]
- JOG3R: Towards 3D-Consistent Video Generators. [[:page_facing_up: Paper](https://arxiv.org/abs/2501.01409)｜[:globe_with_meridians: Project Page](https://paulchhuang.github.io/jog3rwebsite/)]
- GenFusion: Closing the Loop between Reconstruction and Generation via Videos. [[:page_facing_up: Paper](https://arxiv.org/abs/2503.21219) | [:computer: Code](https://github.com/Inception3D/GenFusion)｜[:globe_with_meridians: Project Page](https://genfusion.sibowu.com/)]
- ReVision: High-Quality, Low-Cost Video Generation with Explicit 3D Physics Modeling for Complex Motion and Interaction. [[:page_facing_up: Paper](https://arxiv.org/abs/2504.21855)｜[:globe_with_meridians: Project Page](https://revision-video.github.io/)]

### Video Generation-based Scene Reconstruction

- Geometry Forcing: Marrying Video Diffusion and 3D Representation for Consistent World Modeling. [[:page_facing_up: Paper](https://arxiv.org/abs/2507.07982) | [:computer: Code](https://github.com/CIntellifusion/GeometryForcing)｜[:globe_with_meridians: Project Page](https://geometryforcing.github.io/)]
- Video World Models with Long-term Spatial Memory. [[:page_facing_up: Paper](http://arxiv.org/abs/2506.05284)｜[:globe_with_meridians: Project Page](https://spmem.github.io/)]
- SteerX: Creating Any Camera-Free 3D and 4D Scenes with Geometric Steering. [[:page_facing_up: Paper](https://arxiv.org/abs/2503.12024) | [:computer: Code](https://github.com/byeongjun-park/SteerX)｜[:globe_with_meridians: Project Page](https://byeongjun-park.github.io/SteerX/)]
- 4DNeX: Feed-Forward 4D Generative Modeling Made Easy. [[:page_facing_up: Paper](https://arxiv.org/abs/2508.13154) | [:computer: Code](https://github.com/3DTopia/4DNeX)｜[:globe_with_meridians: Project Page](https://4dnex.github.io/)]
- Lyra: Generative 3D Scene Reconstruction via Video Diffusion Model Self-Distillation. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.19296)]
- ShapeGen4D: Towards High Quality 4D Shape Generation from Videos. [[:page_facing_up: Paper](https://arxiv.org/abs/2510.06208)｜[:globe_with_meridians: Project Page](https://shapegen4d.github.io/)]
- EvoWorld: Evolving Panoramic World Generation with Explicit 3D Memory. [[:page_facing_up: Paper](https://arxiv.org/abs/2510.01183)]
- WorldForge: Unlocking Emergent 3D/4D Generation in Video Diffusion Model via Training-Free Guidance. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.15130)]
- FantasyWorld: Geometry-Consistent World Modeling via Unified Video and 3D Prediction. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.21657)]

## Others

### Panorama

- Splatter-360: Generalizable 360° Gaussian Splatting for Wide-baseline Panoramic Images. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.06250) | [:computer: Code](https://github.com/thucz/splatter360)｜[:globe_with_meridians: Project Page](https://3d-aigc.github.io/Splatter-360/)]
- PanSplat: 4K Panorama Synthesis with Feed-Forward Gaussian Splatting. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.12096) | [:computer: Code](https://github.com/chengzhag/PanSplat)｜[:globe_with_meridians: Project Page](https://chengzhag.github.io/publication/pansplat/)]
- PanoVGGT: Feed-Forward 3D Reconstruction from Panoramic Imagery. [[:page_facing_up: Paper](https://arxiv.org/abs/2603.17571)]

### Localization

- Reloc3r: Large-Scale Training of Relative Camera Pose Regression for Generalizable, Fast, and Accurate Visual Localization. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.23962)]
- A Scene is Worth a Thousand Features: Feed-Forward Camera Localization from a Collection of Image Features. [[:page_facing_up: Paper](https://openreview.net/forum?id=rmDA02o8MV)]
- Multi-View 3D Point Tracking. [[:page_facing_up: Paper](https://arxiv.org/abs/2508.21060)｜[:globe_with_meridians: Project Page](https://ethz-vlg.github.io/mvtracker/)]
- SAIL-Recon: Large SfM by Augmenting Scene Regression with Localization. [[:page_facing_up: Paper](https://arxiv.org/abs/2508.17972) | [:computer: Code](https://github.com/HKUST-SAIL/sail-recon)｜[:globe_with_meridians: Project Page](https://hkust-sail.github.io/sail-recon/)]

### Digital Humans

- Human3R: Everyone Everywhere All at Once. [[:page_facing_up: Paper](https://arxiv.org/abs/2510.06219) | [:computer: Code](https://github.com/fanegg/Human3R)｜[:globe_with_meridians: Project Page](https://fanegg.github.io/Human3R/)]

### Calibration, Inpainting and Reflection

- LoRA3D: Low-Rank Self-Calibration of 3D Geometric Foundation Models. [[:page_facing_up: Paper](https://arxiv.org/abs/2412.07746)｜[:globe_with_meridians: Project Page](https://research.nvidia.com/labs/avg/publication/lu.yang.etal.iclr2025/)]
- BevSplat: Resolving Height Ambiguity via Feature-Based Gaussian Primitives for Weakly-Supervised Cross-View Localization.
- InstaInpaint: Instant 3D-Scene Inpainting with Masked Large Reconstruction Model. [[:page_facing_up: Paper](https://arxiv.org/abs/2506.10980)｜[:globe_with_meridians: Project Page](https://dhmbb2.github.io/InstaInpaint_page/)]
- Reflect3r: Single-View 3D Stereo Reconstruction Aided by Mirror Reflections. [[:page_facing_up: Paper](https://arxiv.org/abs/2509.20607)｜[:globe_with_meridians: Project Page](https://www.robots.ox.ac.uk/ActiveVision/Publications/wu_etal_3dv2025/wu_etal_3dv2025.html)]
