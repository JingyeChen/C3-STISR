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

You can find the rest codes in TPGSR and STT.

# :flushed: Difference between the paper :flushed:

- Visual clue is removed since it does not help improving recognition performance.

- Linguistical clue is trained with CTC loss.

- Performance on CNN is changed from 65.2\%/53.6\%/39.8\% to 65.6\%/53.4\%/39.9\%.
## :wink: Related Works :wink:
· Text Gestalt: Stroke-Aware Scene Text Image Super-Resolution [[Paper]](https://arxiv.org/pdf/2112.08171.pdf) [[Code]](https://github.com/FudanVI/FudanOCR)

· A Text Attention Network for Spatial Deformation Robust Scene Text Image Super-resolution [[Paper]](https://arxiv.org/pdf/2203.09388.pdf) [[Code]](https://github.com/mjq11302010044/TATT)

· Scene Text Telescope: Text-Focused Scene Image Super-Resolution [[Paper]](https://openaccess.thecvf.com/content/CVPR2021/papers/Chen_Scene_Text_Telescope_Text-Focused_Scene_Image_Super-Resolution_CVPR_2021_paper.pdf) [[Code]](https://github.com/FudanVI/FudanOCR)

· Text Prior Guided Scene Text Image Super-resolution [[Paper]](https://arxiv.org/pdf/2106.15368.pdf) [[Code]](https://github.com/mjq11302010044/TPGSR)


## :thumbsup: Special Thanks :thumbsup:
Additionally thank [JingyeChen](https://github.com/JingyeChen) for his help!

Our framework is based on [TPGSR](https://github.com/mjq11302010044/TPGSR), [STT](https://github.com/FudanVI/FudanOCR), and [TG](https://github.com/FudanVI/FudanOCR).

