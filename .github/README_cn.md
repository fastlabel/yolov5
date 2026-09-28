<div align="center">
  <p>
    <a align="center" href="https://ultralytics.com/yolov5" target="_blank">
      <img width="850" src="https://github.com/ultralytics/assets/raw/master/yolov5/v62/splash_readme.png"></a>
    <br><br>
    <a href="https://play.google.com/store/apps/details?id=com.ultralytics.ultralytics_app" style="text-decoration:none;">
      <img src="https://raw.githubusercontent.com/ultralytics/assets/master/app/google-play.svg" width="15%" alt="" /></a>&nbsp;
    <a href="https://apps.apple.com/xk/app/ultralytics/id1583935240" style="text-decoration:none;">
      <img src="https://raw.githubusercontent.com/ultralytics/assets/master/app/app-store.svg" width="15%" alt="" /></a>
  </p>

  [English](../README.md) | 简体中文
  <br>
  <div>
    <a href="https://github.com/ultralytics/yolov5/actions/workflows/ci-testing.yml"><img src="https://github.com/ultralytics/yolov5/actions/workflows/ci-testing.yml/badge.svg" alt="YOLOv5 CI"></a>
    <a href="https://zenodo.org/badge/latestdoi/264818686"><img src="https://zenodo.org/badge/264818686.svg" alt="YOLOv5 Citation"></a>
    <a href="https://hub.docker.com/r/ultralytics/yolov5"><img src="https://img.shields.io/docker/pulls/ultralytics/yolov5?logo=docker" alt="Docker Pulls"></a>
    <br>
    <a href="https://bit.ly/yolov5-paperspace-notebook"><img src="https://assets.paperspace.io/img/gradient-badge.svg" alt="Run on Gradient"></a>
    <a href="https://colab.research.google.com/github/ultralytics/yolov5/blob/master/tutorial.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a>
    <a href="https://www.kaggle.com/ultralytics/yolov5"><img src="https://kaggle.com/static/images/open-in-kaggle.svg" alt="Open In Kaggle"></a>
  </div>

  <br>
   <p>
   YOLOv5🚀是一个在COCO数据集上预训练的物体检测架构和模型系列，它代表了<a href="https://ultralytics.com">Ultralytics</a>对未来视觉AI方法的公开研究，其中包含了在数千小时的研究和开发中所获得的经验和最佳实践。
   </p>

  <div align="center">
    <a href="https://github.com/ultralytics" style="text-decoration:none;">
      <img src="https://github.com/ultralytics/assets/raw/master/social/logo-social-github.png" width="2%" alt="" /></a>
    <img src="https://github.com/ultralytics/assets/raw/master/social/logo-transparent.png" width="2%" alt="" />
    <a href="https://www.linkedin.com/company/ultralytics" style="text-decoration:none;">
      <img src="https://github.com/ultralytics/assets/raw/master/social/logo-social-linkedin.png" width="2%" alt="" /></a>
    <img src="https://github.com/ultralytics/assets/raw/master/social/logo-transparent.png" width="2%" alt="" />
    <a href="https://twitter.com/ultralytics" style="text-decoration:none;">
      <img src="https://github.com/ultralytics/assets/raw/master/social/logo-social-twitter.png" width="2%" alt="" /></a>
    <img src="https://github.com/ultralytics/assets/raw/master/social/logo-transparent.png" width="2%" alt="" />
    <a href="https://www.producthunt.com/@glenn_jocher" style="text-decoration:none;">
      <img src="https://github.com/ultralytics/assets/raw/master/social/logo-social-producthunt.png" width="2%" alt="" /></a>
    <img src="https://github.com/ultralytics/assets/raw/master/social/logo-transparent.png" width="2%" alt="" />
    <a href="https://youtube.com/ultralytics" style="text-decoration:none;">
      <img src="https://github.com/ultralytics/assets/raw/master/social/logo-social-youtube.png" width="2%" alt="" /></a>
    <img src="https://github.com/ultralytics/assets/raw/master/social/logo-transparent.png" width="2%" alt="" />
    <a href="https://www.facebook.com/ultralytics" style="text-decoration:none;">
      <img src="https://github.com/ultralytics/assets/raw/master/social/logo-social-facebook.png" width="2%" alt="" /></a>
    <img src="https://github.com/ultralytics/assets/raw/master/social/logo-transparent.png" width="2%" alt="" />
    <a href="https://www.instagram.com/ultralytics/" style="text-decoration:none;">
      <img src="https://github.com/ultralytics/assets/raw/master/social/logo-social-instagram.png" width="2%" alt="" /></a>
  </div>
</div>


## <div align="center">文件</div>

请参阅[YOLOv5 Docs](https://docs.ultralytics.com)，了解有关训练、测试和部署的完整文件。

## <div align="center">快速开始案例</div>

<details open>
<summary>安装</summary>

在[**Python>=3.9.0**](https://www.python.org/) 的环境中克隆版本仓并安装 [requirements.txt](https://github.com/ultralytics/yolov5/blob/master/requirements.txt)，包括[**PyTorch>=1.13**](https://pytorch.org/get-started/locally/)。
```bash
git clone https://github.com/ultralytics/yolov5  # 克隆
cd yolov5
pip install -r requirements.txt  # 安装
```

</details>

<details open>
<summary>推理</summary>

YOLOv5 [PyTorch Hub](https://github.com/ultralytics/yolov5/issues/36) 推理. [模型](https://github.com/ultralytics/yolov5/tree/master/models) 自动从最新YOLOv5 [版本](https://github.com/ultralytics/yolov5/releases)下载。

```python
import torch

# 模型
model = torch.hub.load('ultralytics/yolov5', 'yolov5s')  # or yolov5n - yolov5x6, custom

# 图像
img = 'https://ultralytics.com/images/zidane.jpg'  # or file, Path, PIL, OpenCV, numpy, list

# 推理
results = model(img)

# 结果
results.print()  # or .show(), .save(), .crop(), .pandas(), etc.
```

</details>

<details>
<summary>用 detect.py 进行推理</summary>

`detect.py` 在各种数据源上运行推理, 其会从最新的 YOLOv5 [版本](https://github.com/ultralytics/yolov5/releases) 中自动下载 [模型](https://github.com/ultralytics/yolov5/tree/master/models) 并将检测结果保存到 `runs/detect` 目录。

```bash
python detect.py --source 0  # 网络摄像头
                          img.jpg  # 图像
                          vid.mp4  # 视频
                          path/  # 文件夹
                          'path/*.jpg'  # glob
                          'https://youtu.be/Zgi9g1ksQHc'  # YouTube
                          'rtsp://example.com/media.mp4'  # RTSP, RTMP, HTTP 流
```

</details>

<details>
<summary>训练</summary>

以下指令再现了 YOLOv5 [COCO](https://github.com/ultralytics/yolov5/blob/master/data/scripts/get_coco.sh)
数据集结果. [模型](https://github.com/ultralytics/yolov5/tree/master/models) 和 [数据集](https://github.com/ultralytics/yolov5/tree/master/data) 自动从最新的YOLOv5 [版本](https://github.com/ultralytics/yolov5/releases) 中下载。YOLOv5n/s/m/l/x的训练时间在V100 GPU上是 1/2/4/6/8天（多GPU倍速）. 尽可能使用最大的 `--batch-size`, 或通过 `--batch-size -1` 来实现 YOLOv5 [自动批处理](https://github.com/ultralytics/yolov5/pull/5092). 批量大小显示为 V100-16GB。

```bash
python train.py --data coco.yaml --cfg yolov5n.yaml --weights '' --batch-size 128
                                       yolov5s                                64
                                       yolov5m                                40
                                       yolov5l                                24
                                       yolov5x                                16
```

<img width="800" src="https://user-images.githubusercontent.com/26833433/90222759-949d8800-ddc1-11ea-9fa1-1c97eed2b963.png">

</details>

<details open>
<summary>教程</summary>

- [训练自定义数据集](https://github.com/ultralytics/yolov5/wiki/Train-Custom-Data) 🚀 推荐
- [获得最佳训练效果的技巧](https://github.com/ultralytics/yolov5/wiki/Tips-for-Best-Training-Results)  ☘️
  推荐
- [多GPU训练](https://github.com/ultralytics/yolov5/issues/475)
- [PyTorch Hub](https://github.com/ultralytics/yolov5/issues/36) 🌟 新
- [TFLite, ONNX, CoreML, TensorRT 输出](https://github.com/ultralytics/yolov5/issues/251) 🚀
- [测试时数据增强 (TTA)](https://github.com/ultralytics/yolov5/issues/303)
- [模型集成](https://github.com/ultralytics/yolov5/issues/318)
- [模型剪枝/稀疏性](https://github.com/ultralytics/yolov5/issues/304)
- [超参数进化](https://github.com/ultralytics/yolov5/issues/607)
- [带有冻结层的迁移学习](https://github.com/ultralytics/yolov5/issues/1314)
- [架构概要](https://github.com/ultralytics/yolov5/issues/6998) 🌟 新
- [使用Weights & Biases 记录实验](https://github.com/ultralytics/yolov5/issues/1289)
- [Roboflow：数据集，标签和主动学习](https://github.com/ultralytics/yolov5/issues/4975) 🌟 新
- [使用ClearML 记录实验](https://github.com/ultralytics/yolov5/tree/master/utils/loggers/clearml) 🌟 新
- [Deci 平台](https://github.com/ultralytics/yolov5/wiki/Deci-Platform) 🌟 新

</details>

## <div align="center">环境</div>

使用经过我们验证的环境，几秒钟就可以开始。点击下面的每个图标了解详情。

<div align="center">
    <a href="https://colab.research.google.com/github/ultralytics/yolov5/blob/master/tutorial.ipynb">
        <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-colab-small.png" width="15%"/>
    </a>
    <a href="https://www.kaggle.com/ultralytics/yolov5">
        <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-kaggle-small.png" width="15%"/>
    </a>
    <a href="https://hub.docker.com/r/ultralytics/yolov5">
        <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-docker-small.png" width="15%"/>
    </a>
    <a href="https://github.com/ultralytics/yolov5/wiki/AWS-Quickstart">
        <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-aws-small.png" width="15%"/>
    </a>
    <a href="https://github.com/ultralytics/yolov5/wiki/GCP-Quickstart">
        <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-gcp-small.png" width="15%"/>
    </a>
</div>

## <div align="center">如何与第三方集成</div>

<div align="center">
  <a href="https://bit.ly/yolov5-deci-platform">
    <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-deci.png" width="10%" /></a>
  <img src="https://github.com/ultralytics/assets/raw/master/social/logo-transparent.png" width="14%" height="0" alt="" />
  <a href="https://cutt.ly/yolov5-readme-clearml">
    <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-clearml.png" width="10%" /></a>
  <img src="https://github.com/ultralytics/assets/raw/master/social/logo-transparent.png" width="14%" height="0" alt="" />
  <a href="https://roboflow.com/?ref=ultralytics">
    <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-roboflow.png" width="10%" /></a>
  <img src="https://github.com/ultralytics/assets/raw/master/social/logo-transparent.png" width="14%" height="0" alt="" />
  <a href="https://wandb.ai/site?utm_campaign=repo_yolo_readme">
    <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-wb.png" width="10%" /></a>
</div>

|Deci ⭐ NEW|ClearML ⭐ NEW|Roboflow|Weights & Biases
|:-:|:-:|:-:|:-:|
|在[Deci](https://bit.ly/yolov5-deci-platform)一键自动编译和量化YOLOv5以提高推理性能|使用[ClearML](https://cutt.ly/yolov5-readme-clearml) (开源!)自动追踪，可视化，以及远程训练YOLOv5|标记并将您的自定义数据直接导出到YOLOv5后，用[Roboflow](https://roboflow.com/?ref=ultralytics)进行训练 |通过[Weights & Biases](https://wandb.ai/site?utm_campaign=repo_yolo_readme)自动跟踪以及可视化你在云端所有的YOLOv5训练运行情况


## <div align="center">为什么选择 YOLOv5</div>

<p align="left"><img width="800" src="https://user-images.githubusercontent.com/26833433/155040763-93c22a27-347c-4e3c-847a-8094621d3f4e.png"></p>
<details>
  <summary>YOLOv5-P5 640 图像 (点击扩展)</summary>

<p align="left"><img width="800" src="https://user-images.githubusercontent.com/26833433/155040757-ce0934a3-06a6-43dc-a979-2edbbd69ea0e.png"></p>
</details>
<details>
  <summary>图片注释 (点击扩展)</summary>

- **COCO AP val** 表示 mAP@0.5:0.95 在5000张图像的[COCO val2017](http://cocodataset.org)数据集上，在256到1536的不同推理大小上测量的指标。
- **GPU Speed** 衡量的是在 [COCO val2017](http://cocodataset.org) 数据集上使用 [AWS p3.2xlarge](https://aws.amazon.com/ec2/instance-types/p3/) V100实例在批量大小为32时每张图像的平均推理时间。
- **EfficientDet** 数据来自 [google/automl](https://github.com/google/automl) ，批量大小设置为 8。
- 复现 mAP 方法: `python val.py --task study --data coco.yaml --iou 0.7 --weights yolov5n6.pt yolov5s6.pt yolov5m6.pt yolov5l6.pt yolov5x6.pt`

</details>

### 预训练检查点

| 模型                                                                                                | 规模<br><sup>(像素) | mAP<sup>验证<br>0.5:0.95 | mAP<sup>验证<br>0.5 | 速度<br><sup>CPU b1<br>(ms) | 速度<br><sup>V100 b1<br>(ms) | 速度<br><sup>V100 b32<br>(ms) | 参数<br><sup>(M) | 浮点运算<br><sup>@640 (B) |
|------------------------------------------------------------------------------------------------------|-----------------------|-------------------------|--------------------|------------------------------|-------------------------------|--------------------------------|--------------------|------------------------|
| [YOLOv5n](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5n.pt)                   | 640                   | 28.0                    | 45.7               | **45**                       | **6.3**                       | **0.6**                        | **1.9**            | **4.5**                |
| [YOLOv5s](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5s.pt)                   | 640                   | 37.4                    | 56.8               | 98                           | 6.4                           | 0.9                            | 7.2                | 16.5                   |
| [YOLOv5m](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5m.pt)                   | 640                   | 45.4                    | 64.1               | 224                          | 8.2                           | 1.7                            | 21.2               | 49.0                   |
| [YOLOv5l](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5l.pt)                   | 640                   | 49.0                    | 67.3               | 430                          | 10.1                          | 2.7                            | 46.5               | 109.1                  |
| [YOLOv5x](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5x.pt)                   | 640                   | 50.7                    | 68.9               | 766                          | 12.1                          | 4.8                            | 86.7               | 205.7                  |
|                                                                                                      |                       |                         |                    |                              |                               |                                |                    |                        |
| [YOLOv5n6](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5n6.pt)                 | 1280                  | 36.0                    | 54.4               | 153                          | 8.1                           | 2.1                            | 3.2                | 4.6                    |
| [YOLOv5s6](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5s6.pt)                 | 1280                  | 44.8                    | 63.7               | 385                          | 8.2                           | 3.6                            | 12.6               | 16.8                   |
| [YOLOv5m6](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5m6.pt)                 | 1280                  | 51.3                    | 69.3               | 887                          | 11.1                          | 6.8                            | 35.7               | 50.0                   |
| [YOLOv5l6](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5l6.pt)                 | 1280                  | 53.7                    | 71.3               | 1784                         | 15.8                          | 10.5                           | 76.8               | 111.4                  |
| [YOLOv5x6](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5x6.pt)<br>+ [TTA][TTA] | 1280<br>1536          | 55.0<br>**55.8**        | 72.7<br>**72.7**   | 3136<br>-                    | 26.2<br>-                     | 19.4<br>-                      | 140.7<br>-         | 209.8<br>-             |

<details>
  <summary>表格注释 (点击扩展)</summary>

- 所有检查点都以默认设置训练到300个时期. Nano和Small模型用 [hyp.scratch-low.yaml](https://github.com/ultralytics/yolov5/blob/master/data/hyps/hyp.scratch-low.yaml) hyps, 其他模型使用 [hyp.scratch-high.yaml](https://github.com/ultralytics/yolov5/blob/master/data/hyps/hyp.scratch-high.yaml).
- **mAP<sup>val</sup>** 值是 [COCO val2017](http://cocodataset.org) 数据集上的单模型单尺度的值。
<br>复现方法: `python val.py --data coco.yaml --img 640 --conf 0.001 --iou 0.65`
- 使用 [AWS p3.2xlarge](https://aws.amazon.com/ec2/instance-types/p3/) 实例对COCO val图像的平均速度。不包括NMS时间（~1 ms/img)
<br>复现方法: `python val.py --data coco.yaml --img 640 --task speed --batch 1`
- **TTA** [测试时数据增强](https://github.com/ultralytics/yolov5/issues/303) 包括反射和比例增强.
<br>复现方法: `python val.py --data coco.yaml --img 1536 --iou 0.7 --augment`

</details>


## <div align="center">分类 ⭐ 新</div>

YOLOv5发布的[v6.2版本](https://github.com/ultralytics/yolov5/releases) 支持训练，验证，预测和输出分类模型！这使得训练分类器模型非常简单。点击下面开始尝试！

<details>
  <summary>分类检查点 (点击展开)</summary>

<br>

我们在ImageNet上使用了4xA100的实例训练YOLOv5-cls分类模型90个epochs，并以相同的默认设置同时训练了ResNet和EfficientNet模型来进行比较。我们将所有的模型导出到ONNX FP32进行CPU速度测试，又导出到TensorRT FP16进行GPU速度测试。最后，为了方便重现，我们在[Google Colab Pro](https://colab.research.google.com/signup)上进行了所有的速度测试。

| 模型                                                                                              | 规模<br><sup>(像素) | 准确度<br><sup>第一 | 准确度<br><sup>前五 | 训练<br><sup>90 epochs<br>4xA100 (小时) | 速度<br><sup>ONNX CPU<br>(ms) | 速度<br><sup>TensorRT V100<br>(ms) | 参数<br><sup>(M) | 浮点运算<br><sup>@224 (B) |
|----------------------------------------------------------------------------------------------------|-----------------------|------------------|------------------|----------------------------------------------|--------------------------------|-------------------------------------|--------------------|------------------------|
| [YOLOv5n-cls](https://github.com/ultralytics/yolov5/releases/download/v6.2/yolov5n-cls.pt)         | 224                   | 64.6             | 85.4             | 7:59                                         | **3.3**                        | **0.5**                             | **2.5**            | **0.5**                |
| [YOLOv5s-cls](https://github.com/ultralytics/yolov5/releases/download/v6.2/yolov5s-cls.pt)         | 224                   | 71.5             | 90.2             | 8:09                                         | 6.6                            | 0.6                                 | 5.4                | 1.4                    |
| [YOLOv5m-cls](https://github.com/ultralytics/yolov5/releases/download/v6.2/yolov5m-cls.pt)         | 224                   | 75.9             | 92.9             | 10:06                                        | 15.5                           | 0.9                                 | 12.9               | 3.9                    |
| [YOLOv5l-cls](https://github.com/ultralytics/yolov5/releases/download/v6.2/yolov5l-cls.pt)         | 224                   | 78.0             | 94.0             | 11:56                                        | 26.9                           | 1.4                                 | 26.5               | 8.5                    |
| [YOLOv5x-cls](https://github.com/ultralytics/yolov5/releases/download/v6.2/yolov5x-cls.pt)         | 224                   | **79.0**         | **94.4**         | 15:04                                        | 54.3                           | 1.8                                 | 48.1               | 15.9                   |
|                                                                                                    |
| [ResNet18](https://github.com/ultralytics/yolov5/releases/download/v6.2/resnet18.pt)               | 224                   | 70.3             | 89.5             | **6:47**                                     | 11.2                           | 0.5                                 | 11.7               | 3.7                    |
| [ResNet34](https://github.com/ultralytics/yolov5/releases/download/v6.2/resnet34.pt)               | 224                   | 73.9             | 91.8             | 8:33                                         | 20.6                           | 0.9                                 | 21.8               | 7.4                    |
| [ResNet50](https://github.com/ultralytics/yolov5/releases/download/v6.2/resnet50.pt)               | 224                   | 76.8             | 93.4             | 11:10                                        | 23.4                           | 1.0                                 | 25.6               | 8.5                    |
| [ResNet101](https://github.com/ultralytics/yolov5/releases/download/v6.2/resnet101.pt)             | 224                   | 78.5             | 94.3             | 17:10                                        | 42.1                           | 1.9                                 | 44.5               | 15.9                   |
|                                                                                                    |
| [EfficientNet_b0](https://github.com/ultralytics/yolov5/releases/download/v6.2/efficientnet_b0.pt) | 224                   | 75.1             | 92.4             | 13:03                                        | 12.5                           | 1.3                                 | 5.3                | 1.0                    |
| [EfficientNet_b1](https://github.com/ultralytics/yolov5/releases/download/v6.2/efficientnet_b1.pt) | 224                   | 76.4             | 93.2             | 17:04                                        | 14.9                           | 1.6                                 | 7.8                | 1.5                    |
| [EfficientNet_b2](https://github.com/ultralytics/yolov5/releases/download/v6.2/efficientnet_b2.pt) | 224                   | 76.6             | 93.4             | 17:10                                        | 15.9                           | 1.6                                 | 9.1                | 1.7                    |
| [EfficientNet_b3](https://github.com/ultralytics/yolov5/releases/download/v6.2/efficientnet_b3.pt) | 224                   | 77.7             | 94.0             | 19:19                                        | 18.9                           | 1.9                                 | 12.2               | 2.4                    |

<details>
  <summary>表格注释 (点击扩展)</summary>

- 所有检查点都被SGD优化器训练到90 epochs, `lr0=0.001` 和 `weight_decay=5e-5`， 图像大小为224，全为默认设置。<br>运行数据记录于 https://wandb.ai/glenn-jocher/YOLOv5-Classifier-v6-2。
- **准确度** 值为[ImageNet-1k](https://www.image-net.org/index.php)数据集上的单模型单尺度。<br>通过`python classify/val.py --data ../datasets/imagenet --img 224`进行复制。
- 使用Google [Colab Pro](https://colab.research.google.com/signup) V100 High-RAM实例得出的100张推理图像的平均**速度**。<br>通过 `python classify/val.py --data ../datasets/imagenet --img 224 --batch 1`进行复制。
- 用`export.py`**导出**到FP32的ONNX和FP16的TensorRT。<br>通过 `python export.py --weights yolov5s-cls.pt --include engine onnx --imgsz 224`进行复制。
</details>
</details>

<details>
  <summary>分类使用实例 (点击展开)</summary>

### 训练
YOLOv5分类训练支持自动下载MNIST, Fashion-MNIST, CIFAR10, CIFAR100, Imagenette, Imagewoof和ImageNet数据集，并使用`--data` 参数. 打个比方，在MNIST上使用`--data mnist`开始训练。

```bash
# 单GPU
python classify/train.py --model yolov5s-cls.pt --data cifar100 --epochs 5 --img 224 --batch 128

# 多-GPU DDP
python -m torch.distributed.run --nproc_per_node 4 --master_port 1 classify/train.py --model yolov5s-cls.pt --data imagenet --epochs 5 --img 224 --device 0,1,2,3
```

### 验证
在ImageNet-1k数据集上验证YOLOv5m-cl的准确性:
```bash
bash data/scripts/get_imagenet.sh --val  # download ImageNet val split (6.3G, 50000 images)
python classify/val.py --weights yolov5m-cls.pt --data ../datasets/imagenet --img 224  # validate
```

### 预测
用提前训练好的YOLOv5s-cls.pt去预测bus.jpg:
```bash
python classify/predict.py --weights yolov5s-cls.pt --data data/images/bus.jpg
```
```python
model = torch.hub.load('ultralytics/yolov5', 'custom', 'yolov5s-cls.pt')  # load from PyTorch Hub
```

### 导出
导出一组训练好的YOLOv5s-cls, ResNet和EfficientNet模型到ONNX和TensorRT:
```bash
python export.py --weights yolov5s-cls.pt resnet50.pt efficientnet_b0.pt --include onnx engine --img 224
```
</details>


## <div align="center">贡献</div>

我们重视您的意见! 我们希望给大家提供尽可能的简单和透明的方式对 YOLOv5 做出贡献。开始之前请先点击并查看我们的 [贡献指南](CONTRIBUTING.md)，填写[YOLOv5调查问卷](https://ultralytics.com/survey?utm_source=github&utm_medium=social&utm_campaign=Survey) 来向我们发送您的经验反馈。真诚感谢我们所有的贡献者!

<!-- SVG image from https://opencollective.com/ultralytics/contributors.svg?width=990 -->
<a href="https://github.com/ultralytics/yolov5/graphs/contributors"><img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/image-contributors-1280.png" /></a>

## <div align="center">联系</div>

关于YOLOv5的漏洞和功能问题，请访问 [GitHub Issues](https://github.com/ultralytics/yolov5/issues)。商业咨询或技术支持服务请访问[https://ultralytics.com/contact](https://ultralytics.com/contact)。

<br>
<div align="center">
  <a href="https://github.com/ultralytics" style="text-decoration:none;">
    <img src="https://github.com/ultralytics/assets/raw/master/social/logo-social-github.png" width="3%" alt="" /></a>
  <img src="https://github.com/ultralytics/assets/raw/master/social/logo-transparent.png" width="3%" alt="" />
  <a href="https://www.linkedin.com/company/ultralytics" style="text-decoration:none;">
    <img src="https://github.com/ultralytics/assets/raw/master/social/logo-social-linkedin.png" width="3%" alt="" /></a>
  <img src="https://github.com/ultralytics/assets/raw/master/social/logo-transparent.png" width="3%" alt="" />
  <a href="https://twitter.com/ultralytics" style="text-decoration:none;">
    <img src="https://github.com/ultralytics/assets/raw/master/social/logo-social-twitter.png" width="3%" alt="" /></a>
  <img src="https://github.com/ultralytics/assets/raw/master/social/logo-transparent.png" width="3%" alt="" />
  <a href="https://www.producthunt.com/@glenn_jocher" style="text-decoration:none;">
    <img src="https://github.com/ultralytics/assets/raw/master/social/logo-social-producthunt.png" width="3%" alt="" /></a>
  <img src="https://github.com/ultralytics/assets/raw/master/social/logo-transparent.png" width="3%" alt="" />
  <a href="https://youtube.com/ultralytics" style="text-decoration:none;">
    <img src="https://github.com/ultralytics/assets/raw/master/social/logo-social-youtube.png" width="3%" alt="" /></a>
  <img src="https://github.com/ultralytics/assets/raw/master/social/logo-transparent.png" width="3%" alt="" />
  <a href="https://www.facebook.com/ultralytics" style="text-decoration:none;">
    <img src="https://github.com/ultralytics/assets/raw/master/social/logo-social-facebook.png" width="3%" alt="" /></a>
  <img src="https://github.com/ultralytics/assets/raw/master/social/logo-transparent.png" width="3%" alt="" />
  <a href="https://www.instagram.com/ultralytics/" style="text-decoration:none;">
    <img src="https://github.com/ultralytics/assets/raw/master/social/logo-social-instagram.png" width="3%" alt="" /></a>
</div>

[assets]: https://github.com/ultralytics/yolov5/releases
[tta]: https://github.com/ultralytics/yolov5/issues/303
