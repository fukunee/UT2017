# 论文大纲

 - 摘要(要把本文的贡献先表述出来,再去做一般性的深度学习文章阐述,最后说明工作内容)
 - 绪论
   - 研究背景(突出小类研究的意义)
   - 国内外研究现状
     - 基于目标识别的按帧处理方法
       - Andrej Karpathy, George Toderici, Sanketh Shetty, Thomas Leung, Rahul Sukthankar, Li Fei-Fei; The IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2014, pp. 1725-1732
     - 基于三维卷积网络的动态模式识别
       - M. Baccouche, F. Mamalet, C. Wolf, C. Garcia, and
       A. Baskurt. Sequential Deep Learning for Human Action
       Recognition. In 2nd International Workshop on Human Behavior
       Understanding (HBU), pages 29–39, Nov. 2011.
       - S. Ji, W. Xu, M. Yang, and K. Yu. 3D convolutional neural
       networks for human action recognition. IEEE Trans. PAMI,
       35(1):221–231, Jan. 2013.
       - A. Karpathy, G. Toderici, S. Shetty, T. Leung, R. Sukthankar,
       and L. Fei-Fei. Large-scale video classification with convolutional neural networks. In Proc. CVPR, pages 1725–1732,
       Columbus, Ohio, USA, 2014.
     - 基于LSTM的长时视频特征提取
       - Yue-Hei Ng J, Hausknecht M, Vijayanarasimhan S, et al. Beyond short snippets: Deep networks for video classification[C]//Proceedings of the IEEE conference on computer vision and pattern recognition. 2015: 4694-4702.
   - 本文研究思路(重点在研究小类,所以选择按帧处理)
   - 本文贡献
     1. 使用视觉显著算法帮助构建数据集
     2. 构建了小类识别数据集
     2. 使用自筛选网络优化数据集
     3. 使用基于图像分割与视觉显著的输入层预处理优化目标识别训练
     4. 使用光流算法优化视频中目标识别准确度
   - 本文结构安排
     - 大课题的综述:1.目标识别 2.深度学习卷积神经网络(含时序神经网络RNN)
     - 本文实验:1.小类数据集 2.FocusNet 3.光流优化FRCNN
     - 总结与展望
 - 卷积神经网络
   - 卷积神经网络基础
     - 神经网络
     - 用神经网络处理图像
     - 典型的简单卷积神经网络
     - 主流的复杂卷积神经网络(根据简单CNN来进行拓展)
       - LeNet
       - AlexNet(Dropout,ReLU)
       - GoogLeNet
       - Inception(!重点)
       - ResNet(!重点)
   - 卷积神经网络对比传统方法的优势
     - 传统特征提取方法的局限性
     - 卷积神经网络在图像任务上获得的成就(综述近年的大赛结果与应用)
   - RNN(!重点)
     - 什么是RNN
     - RNN的结构
     - F-Rcnn的结构与应用
 - 目标识别
   - 目标识别的任务
   - 发展历史综述
   - 基于极深卷积神经网络的目标识别
     - 为什么CNN越来越深?(主要综述在网络加深这个方向上的VGG16-19-MSRANET-RESNET-INCEPTIONRESNET的演进)
     - 比赛中极深网络获得的成果
 - 视觉显著性算法
   - 发展历史
   - 传统视觉显著性算法
   - 基于神经网络的视觉显著性算法
 - 小类数据集及其构建方法(!重点章节)
   - 数据集介绍(模仿PascalVoc数据集论文制作表格和图片并表述)
   - 基于视觉显著性的自动标注
   - 基于深度学习的自筛选网络
 - 专注神经网络FocusNet(!重点章节)
   - 模型介绍(介绍如何让网络更加专注)
   - 网络结构(在ResNet101上进行的修改)
   - 预处理方法(使用视觉显著性与图像分割算法的预处理)
   - 实验结果
 - 基于光流理论优化的F-rcnn的高速网络Context-related F-rcnn
   - 光流理论
   - Context-related F-rcnn(上下文相关的快速RCNN检测网络)
     - 网络结构
     - 实验结果
 - 总结与展望
    - 接下来的工作应该如何进展?
      - 如何将构建数据集的流程自动化
      - 如何针对小类设计模型
      - 如何在不影响准确率的情况下提高对视频的处理速度
    - 成果有什么应用场景?
      - 视频分类
      - 视频检索
      - 视频审核
      - 机器视觉
