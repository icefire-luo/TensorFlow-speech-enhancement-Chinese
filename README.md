[English](https://github.com/linan2/TensorFlow-speech-enhancement.git) | 中文
# 基于深度特征映射的语音增强方法
本项目为可以利用DNN和CNN的方法来进行语音增强，其中DNN使用的三个隐层每个隐层512个节点，CNN使用的是R-CED的网络结构并且加入了一些resnet来防止过拟合。你也可以选择是否使用dropout或者l2等。

## 注意:

[制造数据](https://github.com/linan2/add_reverb2.git) 在运行此代码之前你应该先准备好干净和相应的含噪或者含混响的语音。

如果你的任务是去混响，在运行此代码之前你需要将含混响的语音剪切的和干净的语音一样长。

如果你的任务是做特征增强（不需要还原到语音），你可以把log spectragram特征替换成其他特征（比如MFCC）。

## 使用:
第一步. 运行 ex_trac.sh 来提取 log spectragram 特征.

第二步. 运行 train.sh 来训练和测试模型.

第三步. 运行 ca_pesq.sh 使用PESQ来评价你的结果。

## 补充:
代码还不完善，持续更新ing…

本人在 REVERB challenge 数据集上测试了此代码的效果，PESQ能提高大约0.6—0.8。

过段时间我会继续更新一些比如生成对抗网络、 多任务学习和多目标学习的模型, 一些基于注意力机制的模型也会进行更新,敬请期待…

在解码阶段，您可以选择G&L声码器，也可以使用有噪声的语音原始的相位来合成语音，但是我已经尝试过G&L方法，与原始的相位的使用相比，它不会获得更好的性能。

Email: linanvae@163.com
