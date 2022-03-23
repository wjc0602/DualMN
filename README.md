# DualMN: Dual-branch Memory Network for Visual Object Tracking

### We hope this work will attract more researchers/engineers to build more complete, robust and powerful memory networks for visual object tracking. Code and papers will be released publicly. 


## Abstract
Spatial-temporal memory networks have become the focus of visual object tracking in recent years. Advanced memory networks have achieved outstanding results, but the balance between long-term and short-term memory remains a difficult problem in memory building. Excessive reliance on long-term memory will lead to a poor tracker's ability to discriminate between targets and distractors. Conversely, the tracker cannot adapt to the rapid changes of the target and thus drift. Therefore, we propose the dual-branch memory network(DualMN), which divided the memory network into short-term memory branch and long-term memory branch, cleverly avoids the conflict between them. Specifically, the DualMN consists of a short-term memory branch and a long-term memory branch. The former is dedicated to learning the difference between the new target appearance and the surrounding environment, to better locate the correct target from the complex scene. The latter focuses on learning the essential feature of the target to prevent the drift problem caused by a sudden change in target appearance. During the tracking process, the tracking results of the two branches complement each other. Comprehensive experiments show that DualMN performs favorably against state-of-the-art trackers.

## Architecture

![DualMN](imgs/DualMN.jpg)

#### Install dependencies

* Create and activate a conda environment 
    ```bash
    conda create -n DualMN python=3.8
    conda activate DualMN
    ```  
* Install PyTorch
    ```bash
    conda install -c pytorch pytorch torchvision cudatoolkit=10.0
    ```  

## Acknowledgement
This is a modified version of the python framework [PyTracking](https://github.com/visionml/pytracking) and [video_analyst](https://github.com/MegviiDetection/video_analyst) based on **Pytorch**.

## Contacts
* Jingchao Wang, Collage of Software Engineering, Zhengzhou University of Light Industry, China, 1402994066@qq.com

## Results
We obtain the state-of-the-art results on several benchmarks. 
More results are coming soon. 

<table>
  <tr>
    <th>Model</th>
    <th>OTB<br>Success(%)</th>
    <th>OTB<br>Precision (%)</th>
  </tr>
  <tr>
    <td>Short-term memory</td>
    <td>70.3</td>
    <td>91.0</td>
  </tr>
  <tr>
    <td>Long-term memory</td>
    <td>70.8</td>
    <td>91.9</td>
  </tr>
  <tr>
    <td>Dual-branch memory</td>
    <td>72.1</td>
    <td>92.9</td>
  </tr>
  <tr>
