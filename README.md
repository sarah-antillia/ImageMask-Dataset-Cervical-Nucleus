<h2>ImageMask-Dataset-Cervical-Nucleus (2024/08/30)</h2>

This is ImageMask Dataset for CNSeg (Cervical Nucleus Segmentation).<br>
The dataset used here has been taken from the following kaggle website:<br>
<a href="https://www.kaggle.com/datasets/zhaojing0522/cervical-nucleus-segmentation">
Cervical Nucleus Segmentation
</a>

<br>
<br>
<b>Download ImageMask-Dataset</b><br>
You can download our dataset from the google drive 
<a href="https://drive.google.com/file/d/1Bv0MuqoBEJnWNxUz4gaAAYgNEIocsE9Q/view?usp=sharing">
Cervical-Nucleus-ImageMask-Dataset.zip</a>
<br>


<h3>1. Dataset Citation</h3>
<a href="https://dl.acm.org/doi/abs/10.1016/j.cmpb.2023.107732">
<b>CNSeg: : A dataset for cervical nuclear segmentation</b>
</a>
<br>

<b>Authors:</b><br>
 Jing Zhao, Yong-jun He, Shu-Hang Zhou, Jian Qin, Yi-ning Xie<br>
<br>
@article{ZHAO2023107732, title = {CNSeg: A dataset for cervical nuclear segmentation}, <br>
journal = {Computer Methods and Programs in Biomedicine}, volume = {241}, pages = {107732}, year = {2023}, issn = {0169-2607}, <br>
doi = {https://doi.org/10.1016/j.cmpb.2023.107732}, <br>
url = {https://www.sciencedirect.com/science/article/pii/S016926072300398X}, 
author = {Jing Zhao and Yong-jun He and Shu-Hang Zhou and Jian Qin and Yi-ning Xie} }<br>

<br>
Please see also:<a href="https://github.com/jingzhaohlj/AL-Net">https://github.com/jingzhaohlj/AL-Net</a><br>

You can download CNSeg dataset from the kaggle website:<br>
<a href="https://www.kaggle.com/datasets/zhaojing0522/cervical-nucleus-segmentation">
</a>
<br>
<b>License</b>: Unknown <br>
<br>




<h3>2. ImageMaskDataset Generation</h3>
Please download the master CNSeg dataset from the kaggle web-site.<br> 
<a href="https://www.kaggle.com/datasets/zhaojing0522/cervical-nucleus-segmentation">
Cervical Nucleus Segmentation
</a>
, and expand it in your working directory.
<pre>
./
├─clusteredCell
│  ├─difficult
│  ├─difficult_json
│  ├─normal
│  ├─normal_json
│  ├─sample
│  ├─sample_json
│  ├─test-difficult
│  ├─test-difficult_json
│  ├─test-normal
│  ├─test-normal_json
│  ├─test-sample
│  └─test-sample_json
├─PatchSeg
│  ├─test-images
│  ├─test-labels
│  ├─train-images
│  └─train-labels
├─TargetA
│  ├─test_images
│  ├─test_json
│  └─train_images
└─TargetB
    ├─test-images
    ├─test-labels
    └─train-images
</pre>

<br>
Please run the following command for Python script <a href="./ImageMaskDatasetGenerator.py">
ImageMaskDatasetGenerator.py</a>.
<br>

This command generates two types of datasets from the test and train datasets in PatchSeg.<br>
<pre>
./CNSeg-test-master
├─images
└─masks

./CNSeg-train-master
├─images
└─masks
</pre>

 
<h3>4. Split master</h3>

Pleser run the following command for Python <a href="./split_master.py">split_master.py</a> 
<br>
<pre>
>python split_master.py
</pre>
This creates Cervical-Nucleus-ImageMask-Dataset from CNSeg-test-master and CNSeg-train-master.<br>
<pre>
./Cervical-Nucleus-ImageMask-Dataset
├─test
│  ├─images
│  └─masks
├─train
│  ├─images
│  └─masks
└─valid
    ├─images
    └─masks
</pre>
<hr>
Train images sample<br>
<img src="./asset/train_images_sample.png" width=1024 heigh="auto"><br><br>
Train mask sample<br>
<img src="./asset/train_masks_sample.png" width=1024 heigh="auto"><br><br>


Dataset Statistics <br>
<img src="./Cervical-Nucleus-ImageMask-Dataset_Statistics.png" width="512" height="auto"><br>
