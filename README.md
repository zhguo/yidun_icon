# 易盾图标点选

自动从图片中读取小图标顺序，通过神经网络算法定位图片中全部的图标，然后进行比对确定点选的顺序。提供一张图片即可直接算出最终点选最终结果。

通过率没有细测，用几十张图片肉眼测试，感觉上要比 50% 略高一些。项目大小仅 3M。因为定位的 yolo 算法的网络被压缩到很小，便于下载，执行速度极快。

内附少量样本直接执行 use.py 脚本即可测试，该代码会直接显示标注好的图片。接口方便，代码稍加修改就能拿到自己想要的坐标信息。

```
# 脚本开发于 python3
# 依赖 pytorch：（官网找安装方式，用一个比较新的版本即可）我开发使用版本为 torch-1.4.0-cp36-cp36m-win_amd64.whl
# 依赖 opencv： （用这个安装命令最稳妥 pip install opencv-contrib-python==3.4.1.15 ）
    需要使用sift图像算法，所以注意安装版本。
    建议使用括号内的 pip 安装方式安装，最稳。觉得安装下载慢请增加豆瓣源或清华源的pypi地址
    名字内含有 contrib 的opencv，你简单理解成 opencv 的增强版就行。
```

脚本算法已做简单兼容，兼容 cpu和gpu两个版本。