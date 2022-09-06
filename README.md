# :sparkles: C3-STISR :sparkles:
Official Code for 'C3-STISR: Scene Text Image Super-resolution with Triple Clues'

IJCAI 2022 Accepted Paper 

The code will be gradually open source!

Due to company policy, I can't provide the code. To guarantee reproducibility, I am working on reimplement C3-STISR. The final result will be released around September. Thank you all for your support.

Since a lot of my works (including reviewing papers) are written in one framework, I decide not to release the complete code. Instead, following items are released for reproducibility:

- model scrits

- training scripts

- log

- final pth (accessed via email request)

You can find the rest codes in TPGSR, TATT and STT.

## :e-mail: Contact :e-mail:
Feel free to contact me if you have any problems! zhaomy20@fudan.edu.cn

## :flushed: Difference between the paper :flushed:

- Visual clue is removed since it does not help improving recognition performance.

- Linguistical clue is trained with CTC loss.

- Performance of CRNN is boosted from 65.2\%/53.6\%/39.8\% to 65.6\%/53.4\%/39.9\%.
```bash
evaling easy
[2022-09-05 14:25:13]	PSNR 22.13 | SSIM 0.8532	
save display images
sr_accuray_iter0: 65.60%
lr_accuray: 37.49%
hr_accuray: 76.41%
best_easy = 65.60%*
evaling medium
[2022-09-05 14:25:29]	PSNR 18.98 | SSIM 0.6449	
save display images
sr_accuray_iter0: 53.44%
lr_accuray: 21.40%
hr_accuray: 75.05%
best_medium = 54.43%
evaling hard
[2022-09-05 14:25:45]	PSNR 19.75 | SSIM 0.7125	
save display images
sr_accuray_iter0: 39.91%
lr_accuray: 21.15%
hr_accuray: 64.56%
best_hard = 39.91%*
saving best model
```
## :fire: Training :fire:
```bash
python3 main.py --arch="c3stisr" --test_model="CRNN" --batch_size=48 --STN  --sr_share --gradient  --use_distill --stu_iter=1 --vis_dir='C3-STISR-Final' --mask
```
## :dizzy: Testing :dizzy:
```bash
python3 main.py --arch="c3stisr" --test_model="CRNN" --batch_size=48 --STN  --sr_share --gradient  --use_distill --stu_iter=1 --vis_dir='C3-STISR-Final' --mask --go_test --resume='***'
```
## :punch: Performance :punch: ##
![20220906130237](https://user-images.githubusercontent.com/43022408/188550875-ac52362a-59d8-406a-9c4c-2d90c02d2105.png)

## :satisfied: Citation :satisfied:
If you find this project is useful for your research, please cite:
```
@inproceedings{zhao2022c3,
  title={C3-STISR: Scene Text Image Super-resolution with Triple Clues},
  author={Zhao, Minyi and Wang, Miao and Bai, Fan and Li, Bingjia and Wang, Jie and Zhou, Shuigeng},
  booktitle={IJCAI},
  pages={1707--1713},
  year={2022}
}
```

## :wink: Related Works :wink:
· Text Gestalt: Stroke-Aware Scene Text Image Super-Resolution [[Paper]](https://arxiv.org/pdf/2112.08171.pdf) [[Code]](https://github.com/FudanVI/FudanOCR)

· A Text Attention Network for Spatial Deformation Robust Scene Text Image Super-resolution [[Paper]](https://arxiv.org/pdf/2203.09388.pdf) [[Code]](https://github.com/mjq11302010044/TATT)

· Scene Text Telescope: Text-Focused Scene Image Super-Resolution [[Paper]](https://openaccess.thecvf.com/content/CVPR2021/papers/Chen_Scene_Text_Telescope_Text-Focused_Scene_Image_Super-Resolution_CVPR_2021_paper.pdf) [[Code]](https://github.com/FudanVI/FudanOCR)

· Text Prior Guided Scene Text Image Super-resolution [[Paper]](https://arxiv.org/pdf/2106.15368.pdf) [[Code]](https://github.com/mjq11302010044/TPGSR)


## :thumbsup: Special Thanks :thumbsup:
Additionally thank [JingyeChen](https://github.com/JingyeChen) for his help!

Our framework is based on [TPGSR](https://github.com/mjq11302010044/TPGSR), [STT](https://github.com/FudanVI/FudanOCR), and [TG](https://github.com/FudanVI/FudanOCR).

