# TAC VCamModifer

用于使用图马斯特TAC飞行摇杆来遥控UE中的虚拟相机，这样可以在UE中预览镜头效果，截图或者将镜头轨迹直接通过 Take Record（试拍记录器）记录到Sequencer里面用来编辑和使用。

## 准备工作
- 电脑上安装[图马斯特的TAC飞行摇杆驱动](https://support.thrustmaster.com/zh/product/tca-sidestick-airbus-edition-zh/)
- Unreal Engine项目启用 **Windows RawInput** 插件 和 **VirtualCamera** 插件
- Unreal Engine的项目设定里面导入 Content 目录中的  "Raw Input.ini"，他是适配 TAC飞行摇杆的参数设定。
- 将 VCM_TACModifier.uasset 复制到UE的项目中适当的位置然后重新打开项目，然后打开这个Modifer编译一下。


## 使用方法
- 关卡中添加一个 CineCameraActor
- 在 CineCameraActor 的 Details 面板中增加一个 VCam 组件到 CameraComponent层级下。 ![添加VCam](images/image1.png)
- 在 VCam 的Detail里面的 Modifier Stack里面，增加一个Modifier,名字自己起，Generated Modifer选择"VCM_TACModifer" ![Modifier](images/image2.png)
- Modifier中可配置的参数如下（**应该根据实际的场景大小以及镜头需求来调整，至少前两个很重要**）：
  1. Axis XY Move Speed Factor: 相机水平移动（前后左右）时的速度调节因子
  2. Axis Z Move Speed Factor: 相机垂直移动的速度调节因子
  3. Pitch Move Step:俯仰角的调整步长
  4. Roll Move Step: 翻滚角度的调整步长
  5. Yam Move Gate: 飞行摇杆水平旋转时的门限（摇杆会有偏差，放在那里不动它也可能旋转，根据实际情况来调节这个灵敏度）
  6. Axis Y Move Gate: 水平方向Y轴的灵敏度调节
  7. Axis X Move Gate: 水平方向Z轴的灵敏度调节
  8. Aperture Step: 调整光圈大小的步长
  9. Focus Distance Step: 调整对焦距离的步长
  10. Focal Length Step: 调整焦段的步长

## 摇杆使用方法
具体操作使用参见附图:
![方向控制](images/image3.jpg)
![镜头控制](images/image4.jpg)
![功能按键](images/image5.jpg)