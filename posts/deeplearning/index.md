# 深度学习（yolov5）项目笔记/遇到的问题

## 使用已经训练好的模型

1.在虚拟环境内外安装的库区别很大，虚拟环境内不安装的情况下运行还是会显示模块缺失，无法import库

2.核心问题：在使用自已经训练好的模型进行推理时， Can&#39;t get attribute &#39;DetectionModel&#39;，经排查最后问题是yolo.py版本问题，要注意训练时的yolo.py版本和推理时yolo.py版本是否一致，否则经典报错：
AttributeError: Can&#39;t get attribute &#39;DetectionModel&#39; on &lt;module &#39;models.yolo&#39; from &#39;D:\\DEEPLEARN\\yolov5-mask-42-master\\models\\yolo.py&#39;&gt;

解决办法是git使用git上最新的yolo.py，然而又有新问题：最新的yolo引用了过多的新库。解决办法：将多余的新库在yolo.py中引用处删除，即“手动适配版本”

---

> 作者: Toserhy  
> URL: http://localhost:56904/posts/deeplearning/  

