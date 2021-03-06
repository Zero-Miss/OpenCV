# 凸包(Convex Hull)

## 1 简介

在一个多边形边缘或者内部任意两个点的连线都包含多边形边界或者内部.

- 正式定义:包含集合S中所有点的最小多边形称为凸包.

## 2 检测算法

- Graham扫描法

  - 首先选择Y方向最低的点作为起始点p0
  - 从p0开始极坐标扫描,依次添加p1...pn(排序顺序是根据极坐标的角度大小,逆时针方向)
  - 对每个点pi来说,如果添加pi点到凸包中导致一个左转向(逆时针方向)则添加改点到凸包,反之如果导致一个右转向(顺时针方向)删除改掉从凸包中,如下图所示

  ![graham](image/graham.png)

  

## 3 Opencv API与代码演示

使用convexHull函数.

- 代码演示实现过程;
  -  首先把图像从RGB图像转成灰度
  - 然后再转为二值化图像
  - 再通过发现轮廓得到会选点
  - 凸包API调用
  - 绘制显示

