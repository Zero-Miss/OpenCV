# 亚像素级别角点检测(Python实现)

以上两节学习了harris和Shi-Tomasi角点检测,但是在实际中精度不是很高,所以引入亚像素角点检测.以提高检测精准度.

## 1 作用

- 提高检测精准度

  理论与实际总是不一致的，实际情况几乎所有的角点不会是一个真正的准确像素点.(100,5)实际上(100.126,4.329)．

- 常应用在：跟踪，三维重建和相机矫正

## 2 亚像素定位方法

- 插值方法(取周围点拟合)
- 基于图像距计算
- 曲线拟合方法(高斯曲面,多项式,椭圆曲面)

## 3 代码演示

首先找出角点 是使用Shi-Tomasi实现,然后在做亚像素角点检测.在Opencv中可以使用goodFeaturesToTrack函数找出角点,然后使用  函数你拟合出亚像素级别的角点.在使用实现.具体的代码演示在[Python中](https://github.com/zhi-z/OpenCV/blob/master/OpenCV_Tutorial/FeatureExtraction/CornerDetection/SubpixelCorner/SubpixelCornerDetection.ipynb).

