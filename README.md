# Layout-Guided Novel View Synthesis from a Single Indoor Panorama (CVPR 2021)

## PNVS Dataset
To address the task of panoramic view synthesis, we build a large-scale photo-realistic dataset upon the [Structured3D](https://structured3d-dataset.org/) dataset. We regard the original panoramas in Structured3D as source views, and render 3 target views for each of them. We also manually filter out badly rendered images to ensure the quality of target views. The full dataset (38.5 GB) can be downloaded from this [OneDrive Link](https://shanghaitecheducn-my.sharepoint.com/:u:/g/personal/xujl1_shanghaitech_edu_cn/EU5LNf55F0FEhxoML7eC10YBMdYRGrFqQvXcgrzUPUCJdA?e=ep2AJn). Here is some basic information:  

| Set Name | #Train | #Val | Camera Translation(m) | Resolution |
| :----------: | :----------: | :----------: | :----------: | :----------: |
| easy | 13080 | 1791 | 0.2~0.3 | 512x1024 |
| hard | 17661 | 2279 | 1.0~2.0 | 512x1024 |

After unzipping, the dataset should be organized as follows:

```
<data_root>
└── <set_name>
    └── train.txt
    └── val.txt
    └── source_image
        └── {scene_id}_{room_id}.png
    └── source_depth
        └── {scene_id}_{room_id}.png
    └── source_camera
        └── {scene_id}_{room_id}.txt
    └── source_layout
        └── {scene_id}_{room_id}.txt
    └── target_image
        └── {scene_id}_{room_id}_{index}.png
    └── target_camera
        └── {scene_id}_{room_id}_{index}.txt
```

If you use PNVS dataset in your research, please cite the papers:

```
@inproceedings{Xu_2021_CVPR,
  title     = {Layout-Guided Novel View Synthesis From a Single Indoor Panorama},
  author    = {Xu, Jiale and Zheng, Jia and Xu, Yanyu and Tang, Rui and Gao, Shenghua},
  booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
  year      = {2021},
}
@inproceedings{Structured3D,
  title     = {Structured3D: A Large Photo-realistic Dataset for Structured 3D Modeling},
  author    = {Jia Zheng and Junfei Zhang and Jing Li and Rui Tang and Shenghua Gao and Zihan Zhou},
  booktitle = {Proceedings of The European Conference on Computer Vision (ECCV)},
  year      = {2020}
}
```
