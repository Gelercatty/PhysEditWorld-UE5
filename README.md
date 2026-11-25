# PhysEditWorld-UE5

Unreal Engine 5 toolkit for recording, replaying, and rendering controlled physics experiments for **PhysEditWorld: A Large-Scale Dataset Toward Physics-Editable World Models**.

[Paper (arXiv)](https://arxiv.org/abs/2606.26694) · [Project page and videos](https://yizhiqianbi.github.io/physeditworld/) · [Dataset (ModelScope)](https://www.modelscope.cn/datasets/GelerCAT/PhysicalWorld)

## Matched replay

A matched replay starts with a single recorded action trace. Each run uses the same initial state, character controller, action sequence, and camera policy, with a different gravity multiplier. The pipeline renders synchronized views and exports frame and replay metadata so that runs can be compared across gravity settings.

## Release status

This repository currently hosts the project overview. The code and runnable demo are in preparation for Unreal Engine 5.7.

| Component | Planned release |
| --- | --- |
| UE Editor plugin | Tools to prepare a scene, inspect navigation paths, record action traces, and configure replay and rendering. |
| Linux batch tools | Scripts to validate replay plans, run headless Unreal Editor jobs, and encode rendered frames into videos. |
| Rollout demo | A Classroom example that replays one route at **0.5× and 1.0× gravity**. Each run is 20 seconds at 30 fps, with eight camera views at 1280 × 720. |

The project page shows matched rollouts from the dataset. Setup instructions and commands for the Classroom example will accompany the code release.

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
