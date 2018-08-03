### udacity DLND Project 5 :Face generation.


  在该项目中，将使用对抗生成神经网络（GAN）生成新的人脸图像，具体采用了深度卷积生成对抗网络结构（DCGAN）。<br>
  如果想要更好的训练效果，请参考训练GAN的经验总结：https://github.com/soumith/ganhacks<br>
  该项目使用了：mnist数据集http://yann.lecun.com/exdb/mnist/ ；<br>
  CelebA人脸数据集http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html 。<br>


注意我们的参数最好设置成2的倍数，比如4、8、16、32、64。这样可以让tensorflow在计算的时候进行优化，让你的模型训练更加迅速。Batch size 主要影响的是你GAN生成的图片质量，下面给你一些关于参数设置的建议：<br>
* 对于celeA这个数据集来说，由于它包含了许多大图像，所以Batch size设置为16或者32比较合适。
* 对于MNIST这个数据集来说，图像相对较小，只是28 * 28 的黑白色图形，所以Batch size 设置为32 或者64都是可以的。
* 在GAN中，learning rate 设置为0.0002应该不错，但是有些稍微提高一点能够有效地减少你训练的时间（0.001左右）。
* Beta 在0.5或0.4左右的话，也不错。你可以尝试着调整一下这些参数，应该能得到不错的效果。
* z dim一般设置为100比较好～


