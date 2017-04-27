# 论文大纲

 - 摘要(要把本文的贡献先表述出来,再去做一般性的深度学习文章阐述,最后说明工作内容)
 - 绪论
   - 研究背景(突出小类研究的意义)
   - 国内外研究现状
     - 基于目标识别的按帧处理方法
       - Karpathy A, Toderici G, Shetty S, et al. Large-scale video classification with convolutional neural networks[C]//Proceedings of the IEEE conference on Computer Vision and Pattern Recognition. 2014: 1725-1732.
     - 基于三维卷积网络的动态模式识别
       - M. Baccouche, F. Mamalet, C. Wolf, C. Garcia, and
       A. Baskurt. Sequential Deep Learning for Human Action
       Recognition. In 2nd International Workshop on Human Behavior
       Understanding (HBU), pages 29–39, Nov. 2011.
       - S. Ji, W. Xu, M. Yang, and K. Yu. 3D convolutional neural
       networks for human action recognition. IEEE Trans. PAMI,
       35(1):221–231, Jan. 2013.
     - 基于LSTM的长时视频特征提取
       - Yue-Hei Ng J, Hausknecht M, Vijayanarasimhan S, et al. Beyond short
       snippets: Deep networks for video classification[C]//Proceedings of the IEEE conference on computer vision and pattern recognition. 2015: 4694-4702.
   - 本文研究思路(重点在研究小类,所以选择按帧处理)
   - 本文贡献
     1. 使用视觉显著算法帮助构建数据集
     2. 构建了小类识别数据集
     2. 使用自筛选网络优化数据集
     3. 使用基于图像分割与视觉显著的输入层预处理优化目标识别训练
     4. 使用光流算法优化视频中目标识别准确度
   - 本文结构安排
     - 大课题的综述:1.目标识别 2.深度学习卷积神经网络(基于区域的神经网络RCNN)
     - 本文实验:1.小类数据集 2.FocusNet 3.光流优化FRCNN
     - 总结与展望
 - 卷积神经网络
   - 卷积神经网络基础
     - 神经网络(从最基本的机器学习内容去引入概念,参考我的笔记)
       - logistic regression
       - 梯度下降算法
       - 反向传播算法
         - Goodfellow I, Bengio Y, Courville A. Deep learning[M]. MIT Press, 2016.
     - 用神经网络处理图像
       - LeCun Y, Boser B E, Denker J S, et al. Handwritten digit recognition with a back-propagation network[C]//Advances in neural information processing systems. 1990: 396-404.
     - 典型的简单卷积神经网络
       - LeCun Y, Bengio Y. Convolutional networks for images, speech, and
       time series[J]. The handbook of brain theory and neural networks, 1995, 3361(10): 1995.
     - 主流的复杂卷积神经网络(根据简单CNN来进行拓展)
       - AlexNet(Dropout,ReLU)
         - Krizhevsky A, Sutskever I, Hinton G E. Imagenet classification with deep convolutional neural networks[C]//Advances in neural information processing systems. 2012: 1097-1105.
       - GoogLeNet(inceptionV1)(!重点)
         - Szegedy C, Liu W, Jia Y, et al. Going deeper with convolutions[C]//Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition. 2015: 1-9.
       - InceptionV2BN(!重点)
         - Ioffe S, Szegedy C. Batch normalization: Accelerating deep network training by reducing internal covariate shift[J]. arXiv preprint arXiv:1502.03167, 2015.
       - InceptionV3Rethinking(!重点)
         - Szegedy C, Vanhoucke V, Ioffe S, et al. Rethinking the inception architecture for computer vision[C]//Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition. 2016: 2818-2826.
       - InceptionV4Inception-ResNet(!重点)
         - Szegedy C, Ioffe S, Vanhoucke V, et al. Inception-v4, inception-resnet and the impact of residual connections on learning[J]. arXiv preprint arXiv:1602.07261, 2016.
   - 基于卷积神经网络的图像处理
     - 传统特征提取方法 vs CNN
       - SIFT/SURF
         - Lowe D G. Distinctive image features from scale-invariant keypoints[J]. International journal of computer vision, 2004, 60(2): 91-110.
         - Bay H, Tuytelaars T, Van Gool L. Surf: Speeded up robust features[J]. Computer vision–ECCV 2006, 2006: 404-417.
       - HOG
         - Dalal N, Triggs B. Histograms of oriented gradients for human detection[C]//Computer Vision and Pattern Recognition, 2005. CVPR 2005. IEEE Computer Society Conference on. IEEE, 2005, 1: 886-893.
       - 什么是End2End?让黑箱解决一切
         - Wieschollek P, Schölkopf B, Lensch H, et al. End-to-end learning for image burst deblurring[J]. arXiv preprint arXiv:1607.04433, 2016.
         - Bojarski M, Del Testa D, Dworakowski D, et al. End to end learning for self-driving cars[J]. arXiv preprint arXiv:1604.07316, 2016.
     - 卷积神经网络在图像任务上获得的成就(综述近年的大赛结果与应用)
       - ILSVRC2016
   - RCNN(!重点)
     - 什么是RCNN
     - RNN的结构
     - F-Rcnn的结构与应用
       - Girshick R, Donahue J, Darrell T, et al. Rich feature hierarchies
       for accurate object detection and semantic segmentation[C]//
       Proceedings of the IEEE conference on computer vision and pattern
       recognition. 2014: 580-587.
       - Ren S, He K, Girshick R, et al. Faster r-cnn: Towards real-time object
       detection with region proposal networks[C]//Advances in neural
       information processing systems. 2015: 91-99.
       - Girshick R. Fast r-cnn[C]//Proceedings of the IEEE International
       Conference on Computer Vision. 2015: 1440-1448.
 - 目标检测
   - 目标检测的比赛及其结果
     - Large Scale Visual Recognition Challenge
   - 基于极深卷积神经网络的目标识别
     - 为什么CNN越来越深?(主要综述在网络加深这个方向上的VGG16-19-MSRANET-RESNET-INCEPTIONRESNET的演进)
       - Simonyan, K. and A. Zisserman (2014). "Very deep convolutional networks for large-scale image recognition." arXiv preprint arXiv:1409.1556.
       - He, K., et al. (2016). Deep residual learning for image recognition. Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition.
       - He K, Zhang X, Ren S, et al. Identity mappings in deep residual networks[C]//European Conference on Computer Vision. Springer International Publishing, 2016: 630-645.
   - 视频目标检测
     - Object detection from video, VID
 - 机器视觉注意力模型
   - 发展历史
     - Borji A, Itti L. State-of-the-art in visual attention modeling.[J]. IEEE Transactions on Pattern Analysis & Machine Intelligence, 2013, 35(1):185-207.
   - 传统注意力模型
     - Borji A, Itti L. State-of-the-art in visual attention modeling.[J]. IEEE Transactions on Pattern Analysis & Machine Intelligence, 2013, 35(1):185-207.
   - 基于神经网络的注意力模型
 - 小类数据集及其构建方法(!重点章节)
   - 数据集介绍(模仿PascalVoc数据集论文制作表格和图片并表述)
     - Everingham M, Van Gool L, Williams C K I, et al. The pascal visual object classes (voc) challenge[J]. International journal of computer vision, 2010, 88(2): 303-338.
   - 基于注意力模型的自动标注
   - 基于深度学习的自筛选网络
 - 专注神经网络FocusNet(!重点章节)
   - 模型介绍(介绍如何让网络更加专注)
   - 网络结构(在ResNet101上进行的修改)
   - 预处理方法(使用视觉显著性与图像分割算法的预处理)
   - 实验结果
 - 基于光流理论优化的F-rcnn的高速网络Context-related F-rcnn
   - 光流理论
     - Horn B K P, Schunck B G. Determining optical flow[J]. Artificial intelligence, 1981, 17(1-3): 185-203.
     - Weinzaepfel P, Revaud J, Harchaoui Z, et al. Deepflow: Large displacement optical flow with deep matching[C]//Proceedings of the IEEE International Conference on Computer Vision. 2013: 1385-1392.
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
