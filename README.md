# 标注自己的数据集，训练、评估、测试、部署自己的算法

代码测试[云GPU环境](https://www.runpod.io/)：GPU RTX 3070、CUDA v11.8

![计算机视觉解决的基本问题](https://unc-s3.jongun2038.win/cv_fund.png)

```sh
yolo detect predict model=yolov8n.pt source=0 show

    TASK     MODE       MODELS           ARGS
    detect   train      yolov8n.pt        2c.jpg
    segment  val        yolov8s.pt        shuffle.mp4
    classify predict    yolov8m.pt        0
    pose     export     yolov8l.pt        images/
             track      yolov8x.pt        https://ultralytics.com/images/bus.jpg
             benchmark  yolov8n-cls.pt    https://youtu.be/Zgi9g1ksQHc
                        yolov8s-cls.pt    rtsp://example.com/media.mp4
                        yolov8m-cls.pt
                        yolov8l-cls.pt
                        yolov8x-cls.pt
    
                        yolov8n-seg.pt
                        yolov8s-seg.pt
                        yolov8m-seg.pt
                        yolov8l-seg.pt
                        yolov8x-seg.pt
                        
                        yolov8n-obb.pt
                        yolov8s-obb.pt
                        yolov8m-obb.pt
                        yolov8l-obb.pt
                        yolov8x-obb.pt

                        yolov8n-pose.pt
                        yolov8s-pose.pt
                        yolov8m-pose.pt
                        yolov8l-pose.pt
                        yolov8x-pose.pt
                        yolov8x-pose-p6.pt
```

## 图像分类

### 构建自己的图像分类数据集

收集图像、下载样例数据集，删除系统多余文件，划分训练集、测试集，统计图像尺寸、比例分布、拍照地点位置分布，统计各类别图像数量

### 【Pytorch】ImageNet预训练图像分类模型预测

使用Pytorch自带的预训练图像分类模型，分别对单张图像、视频、摄像头实时画面运行图像分类预测

### 【Pytorch】迁移学习Fine-tuning训练自己的图像分类模型

### 【Pytorch】用训练得到的pytorch图像分类模型，识别图像、视频、摄像头画面

### 测试集评估

计算各类别分类评估指标，绘制混淆矩阵、PR曲线、ROC曲线。

### 测试集语义特征降维可视化

抽取Pytorch训练得到的图像分类模型中间层的输出特征，作为输入图像的语义特征。计算测试集所有图像的语义特征，使用t-SNE和UMAP两种降维方法降维至二维和三维，可视化。

### 可解释性分析、显著性分析

CAM热力图系列算法

## 单目标追踪（蜜蜂追踪）

## 视频人流量计数+足迹追踪

## 生成式大模型

## OCR文字识别

## 多模态数据的处理与融合技术，图像、文本、语音等不同模态数据的联合建模方法
