#ssd中用到了比较独特的数据增强方法，尤其是随机裁剪和之前的方式不太一样，现在通过读源码，用python重新实现了一遍，先记下来

#同为数据增强，ssd的用法有点不太一样，特别是random crop随机裁剪
ssd的方法有放大有缩小

随机裁剪的时候也并没有太多的考虑目标主体是否落在了裁剪框里面，比如一个人的图片，如果神展开四肢，这个人的ground truth会比较大，但就目标来讲，有点稀疏矩阵的感觉。

所以，代码jaccard就是再次实现这个方法（单纯的预处理）。
