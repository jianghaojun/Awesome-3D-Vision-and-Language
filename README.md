# Awesome-3D-Visual-Grounding [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/jianghaojun/Awesome-3D-Visual-Grounding)

A curated list of research papers in 3D visual grounding. 

**Update on 2022/04/15: Create this repository.**

## Table of Contents

- [3D-VG Datasets](#datasets)
- [3D-VG Paper Roadmap (Chronological Order)](#paper-roadmap-chronological-order)
- [3D-VG Workshops](#workshops)
- [Point Cloud Papers](#point-cloud-papers)
- [Contacts](#contacts)

<!-- 1. First Author. **Paper Name**. Conf. [[Paper]]() [[Code]]() [[Website]]() -->

## Datasets
1. **ReferIt3D**(**Nr3D**, **Sr3D/Sr3D+**): Achlioptas, Panos, et al. **ReferIt3D: Neural Listeners for Fine-Grained 3D Object Identification in Real-World Scenes**. ECCV 2020, <font color=Red>**Oral**</font>. [[Paper]](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123460409.pdf) [[Code]](https://github.com/referit3d/referit3d) [[Website]](https://referit3d.github.io/) [[Leaderboard]](https://referit3d.github.io/benchmarks.html)
2. **ScanRefer**: Chen, Dave Zhenyu, et al. **ScanRefer 3D Object Localization in RGB-D Scans Using Natural Language**. ECCV 2020. [[Paper]](https://arxiv.org/abs/1912.08830) [[Code]](https://github.com/daveredrum/ScanRefer) [[Website]](https://daveredrum.github.io/ScanRefer/) [[Leaderboard]](http://kaldir.vc.in.tum.de/scanrefer_benchmark/)

    **Dataset Statistics**: 
    - On average, there are 13.81 objects, 64.48 descriptions per scene, and 4.67 descriptions per object.
    - Average length of descriptions is 20.27. Frequency of object attributes: spatial language (98.7%), color (74.7%), shape terms (64.9%), and size information (14.2%).

## Paper Roadmap (Chronological Order)
### ECCV 2020
1. Achlioptas, Panos, et al. **ReferIt3D: Neural Listeners for Fine-Grained 3D Object Identification in Real-World Scenes**. ECCV 2020, <font color=Red>**Oral**</font>. [[Paper]](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123460409.pdf) [[Code]](https://github.com/referit3d/referit3d) [[Website]](https://referit3d.github.io/)
2. Chen, Dave Zhenyu, et al. **ScanRefer 3D Object Localization in RGB-D Scans Using Natural Language**. ECCV 2020. [[Paper]](https://arxiv.org/abs/1912.08830) [[Code]](https://github.com/daveredrum/ScanRefer) [[Website]](https://daveredrum.github.io/ScanRefer/)

### AAAI 2021
1. Huang, Pin-Hao, et al. **Text-guided graph neural networks for referring 3d instance segmentation**. AAAI 2021. [[Paper]](https://ojs.aaai.org/index.php/AAAI/article/view/16253) [[Code]](https://github.com/hanhung/TGNN)

### CVPR 2021
1. Feng, Mingtao, et al. **Free-form Description Guided 3D Visual Graph Network for Object Grounding in Point Cloud**. CVPR 2021. [[Paper]](https://arxiv.org/abs/2103.16381) [[Code]](https://github.com/PNXD/FFL-3DOG)
2. Liu, Haolin, et al. **Refer-It-in-RGBD: A Bottom-Up Approach for 3D Visual Grounding in RGBD Images**. CVPR 2021. [[Paper]](https://arxiv.org/abs/2103.07894) [[Code]](https://github.com/UncleMEDM/Refer-it-in-RGBD) [[Website]](https://unclemedm.github.io/Refer-it-in-RGBD/)

### ICCV 2021
1. Yang, Zhengyuan, et al. **SAT: 2D Semantics Assisted Training for 3D Visual Grounding**. ICCV 2021, <font color=Red>**Oral**</font>. [[Paper]](https://arxiv.org/abs/2105.11450) [[Code]](https://github.com/zyang-ur/SAT)

    **Personal Notes**: 
    - Use corresponding 2D image data(ROI feature, label, bbox coordinates and camera pose) to assist 3D grounding.
    - Very solid experiments.

2. Yuan, Zhihao, et al. **InstanceRefer: Cooperative Holistic Understanding for Visual Grounding on Point Clouds through Instance Multi-level Contextual Referring** . ICCV 2021. [[Paper]](https://arxiv.org/abs/2103.01128) [[Code]](https://github.com/CurryYuan/InstanceRefer)
3. Zhao, Lichen, et al. **3DVG-Transformer: Relation modeling for visual grounding on point clouds**. ICCV 2021. [[Paper]](https://openaccess.thecvf.com/content/ICCV2021/papers/Zhao_3DVG-Transformer_Relation_Modeling_for_Visual_Grounding_on_Point_Clouds_ICCV_2021_paper.pdf) [[Code]](https://github.com/zlccccc/3DVG-Transformer)

    **Personal Notes**: 
    - The novelty of this paper comes from the coordinate-guied contextual aggregation module.

### ACM-MM 2021
1. He, Dailan, et al. **TransRefer3D: Entity-and-Relation Aware Transformer for Fine-Grained 3D Visual Grounding**. ACM-MM 2021. [[Paper]](https://arxiv.org/abs/2108.02388)

### CVPR 2022
1. Huang, Shijia, et al. **Multi-View Transformer for 3D Visual Grounding**. CVPR 2022. [[Paper]](https://arxiv.org/abs/2204.02174) [[Code]](https://github.com/sega-hsj/MVT-3DVG)

    **Personal Notes**: 
    - Rotating the center xyz of objects to provide view-related positional information before going through a Tranformer decoder. 
    - Strong results on Nr3D and Sr3D, good reuslts on ScanRefer.

2. Luo, Junyu, et al. **3D-SPS: Single-Stage 3D Visual Grounding via Referred Point Progressive Selection**. CVPR 2022, <font color=Red>**Oral**</font>. [[Paper]](https://arxiv.org/abs/2204.06272) [[Code]](https://github.com/fjhzhixi/3D-SPS)
    
    **Personal Notes**: 
    - First single stage work in 3D Visual Grounding !!!
    - The general idea is similar to the iterative shrinking work in 2D Visual Grounding, but the design is more elegant.

3. Cai, Daigang, et al. **3DJCG: A Unified Framework for Joint Dense Captioning and Visual Grounding on 3D Point Clouds**. CVPR 2022.


## Workshops
1. CVPR 2021 1st Workshop on Language for 3D Scenes. [[Website]](https://language3dscenes.github.io/)
  
## Point Cloud Papers


## Contacts
jhj20 at mails dot tsinghua dot edu dot cn
