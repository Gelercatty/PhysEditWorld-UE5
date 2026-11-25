# PhysEditWorld-UE5

**PhysEditWorld: A Large-Scale Dataset Toward Physics-Editable World Models**

Unreal Engine 5 toolkit for recording, replaying, and rendering controlled physics experiments.

[Paper](https://arxiv.org/abs/2606.26694) · [Project page and videos](https://yizhiqianbi.github.io/physeditworld/) · [Dataset on ModelScope](https://www.modelscope.cn/datasets/GelerCAT/PhysicalWorld)

[![ModelScope dataset downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fwww.modelscope.cn%2Fopenapi%2Fv1%2Fdatasets%2FGelerCAT%2FPhysicalWorld&query=%24.data.downloads&label=Dataset+downloads&color=1677ff&cacheSeconds=3600)](https://www.modelscope.cn/datasets/GelerCAT/PhysicalWorld)

![Figure 1 from the PhysEditWorld paper showing the matched replay pipeline and its synchronized outputs](https://arxiv.org/html/2606.26694v2/Teaser.png)

## Abstract

PhysEditWorld is a multimodal dataset for studying how game world models respond when a physical parameter changes. The initial release focuses on gravity. The UE5 pipeline records an action trace once and replays it at several gravity levels while holding the scene, initial state, controller, and camera policy fixed. The resulting matched rollouts let researchers compare motion under controlled gravity changes.

The dataset covers **12 UE5 scenes**, **100+ hours of gameplay interactions**, and **60M+ rendered frames**. It pairs synchronized multi-view rendering with depth, normals, audio, action traces, camera trajectories, engine states, semantic annotations, and gravity labels. The paper reports that training with PhysEditWorld improves gravity-sensitive motion generation and gravity understanding.

[Read the full abstract on arXiv](https://arxiv.org/abs/2606.26694)

## Open-source checklist

- [x] Publish the dataset on ModelScope.
- [ ] Release the UE 5.7 Editor plugin for scene preparation, action recording, and replay configuration.
- [ ] Release the Linux batch tools for plan validation, headless replay and rendering, and video encoding.
- [ ] Release a runnable **Third Person** rollout demo that replays the same movement and jump inputs at **0.5× and 1.0× gravity**.

The demo uses the standard UE 5.7 **Third Person** template with **Variant** set to **None**. Setup and replay instructions will accompany the toolkit. [Epic’s Third Person template guide](https://dev.epicgames.com/documentation/en-us/unreal-engine/third-person-template-in-unreal-engine?application_version=5.7)

## Citation

If you use this toolkit or the dataset in your research, please cite the paper.

```bibtex
@misc{hu2026physeditworldlargescaledatasetphysicseditable,
  title         = {PhysEditWorld: A Large-Scale Dataset Toward Physics-Editable World Models},
  author        = {Bin Hu and Yanwen Ma and Jiehui Huang and Ziliang Zhang and
                   Haoning Wu and Ruicheng Zhang and Yaokun Li and Zijun Wang and
                   Yuechen Zhang and Chun-Mei Tseng and Hanhui Li and Shengju Qian and
                   Jun Zhou and Kaipeng Zhang and Xiaodan Liang and Jiaya Jia and Xiu Li},
  year          = {2026},
  eprint        = {2606.26694},
  archivePrefix = {arXiv},
  primaryClass  = {cs.CV},
  url           = {https://arxiv.org/abs/2606.26694}
}
```
