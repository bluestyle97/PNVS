# Layout-Guided Novel View Synthesis from a Single Indoor Panorama (CVPR 2021)

## PNVS Dataset
To address the task of panoramic view synthesis, we build a large-scale photo-realistic dataset upon the [Structured3D](https://structured3d-dataset.org/) dataset. We regard the original panoramas in Structured3D as source views, and render 3 target views for each of them. We also manually filter out badly rendered images to ensure the quality of target views. The full dataset (38.5 GB) can be downloaded from this [OneDrive Link](https://shanghaitecheducn-my.sharepoint.com/:u:/g/personal/xujl1_shanghaitech_edu_cn/EU5LNf55F0FEhxoML7eC10YBMdYRGrFqQvXcgrzUPUCJdA?e=ep2AJn). Here is some basic information:  

| Set Name | #Train | #Val | Camera Translation(m) | Resolution |
| :----------: | :----------: | :----------: | :----------: | :----------: |
| easy | 13080 | 1791 | 0.2~0.3 | 512x1024 |
| hard | 17661 | 2279 | 1.0~2.0 | 512x1024 |

After unzipping, the dataset should be organized as follows:

```
├── <data_root>
│   └── <set_name>
│       └── train.txt
│       └── val.txt
│       └── source_image
│           └── {scene_id}_{room_id}.png
│       └── source_depth
│           └── {scene_id}_{room_id}.png
│       └── source_camera
│           └── {scene_id}_{room_id}.txt
│       └── source_layout
│           └── {scene_id}_{room_id}.txt
│       └── target_image
│           └── {scene_id}_{room_id}_{index}.png
│       └── target_camera
│           └── {scene_id}_{room_id}_{index}.txt
```

If you use PNVS dataset in your research, please cite the papers:

```
@inproceedings{xu2021layout,
  title={Layout-Guided Novel View Synthesis from a Single Indoor Panorama},
  author={Xu, Jiale and Zheng, Jia and Xu, Yanyu and Tang, Rui and Gao, Shenghua},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  pages={16438--16447},
  year={2021}
}
@inproceedings{zheng2020structured3d,
  title={Structured3d: A large photo-realistic dataset for structured 3d modeling},
  author={Zheng, Jia and Zhang, Junfei and Li, Jing and Tang, Rui and Gao, Shenghua and Zhou, Zihan},
  booktitle={Computer Vision--ECCV 2020: 16th European Conference, Glasgow, UK, August 23--28, 2020, Proceedings, Part IX 16},
  pages={519--535},
  year={2020},
  organization={Springer}
}
```
