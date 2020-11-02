# UE4 课程

## 0. 介绍

* 放风筝的小男孩
* 游戏
* 建筑
* 影视
* 广播
* UE5

## 1.	关卡设计师入门

* 新建一个“游戏”项目
* 选择模板“第三人称游戏”
    * Third Person 第三人称
    * First Person 第一人称
* 项目设置选择
    * 蓝图
    * 桌面/主机
    * 最高质量
    * 含初学者内容包
    * 已禁用光线追踪

打开 /Content/StarterContent/Maps/StarterMap

* Actor
* Pawn
* Static Mesh 静态网格体.
* Player Start 玩家出生点
* 光源
    * Directional Light（定向光源）
    * Point Light（点光）
    * Spot Light（聚光）
    * Sky Light（天光）
* 光照
    * 静态光照
    * Static Lighting Level Scale 静态光照等级范围
    * Num Indirect Lighting Bounces 间接光照反射数

https://docs.unrealengine.com/zh-CN/Engine/QuickStart/index.html

## 2.	蓝图的Hello World

* ### Hello World 蓝图
    * 在场景中创建一个“空Actor”
    * 点击 “蓝图/添加脚本”
    
       ![输入图片说明](https://images.gitee.com/uploads/images/2020/1021/122701_fdec4f4c_792465.png "1.png")
    
    * 命名为 "BPHelloWorld"
    * 添加组件 "Box Collision"
    * 为 "Box" 添加事件
        * 组件开始重叠时
        * 组件结束重叠时
    * 添加 "Print" 函数

* ### 让火变得更大
    * 为粒子系统Fire添加Box Collision
    * Set Scale 设置缩放

<br>

--------------------------
### <i>作业：灭火人</i>
- 使用StarterContent
- 创建一块地
- 创建一些触碰就会熄灭的火球
--------------------------
<br>

## 3. Landscape and Foliage 地形与植物
* Landscape
    * 创建地形
    * 编辑地形
* Foliage
    * 添加树木 草 石头

## 4.	使用蓝图控制

创建一个新“空工程”，来做一个滚动的球

* ### 创建一个灯光控制 (Actor)
  * 创建一个立方体做为“地板按钮”
  * 创建一个 Box Collision
  * 创建一个光源 (Spot Light 或者 Point Light)

  ![输入图片说明](https://images.gitee.com/uploads/images/2020/1021/001410_d22693e1_792465.png "微信图片_20201021001356.png")

  * 控制灯光开关
    * 了解：注释
    * 了解：branch(if)
    * 了解：Boolean

  ![输入图片说明](https://images.gitee.com/uploads/images/2020/1021/001615_ed42e360_792465.png "微信图片_20201021001547.png")

  * 控制灯光颜色

  ![输入图片说明](https://images.gitee.com/uploads/images/2020/1021/001741_4227ea58_792465.png "coolo.png")

* ### 创建一个玩家可以控制的滚动的球 (Pawn)
  * 创建一个Pawn蓝图, 取名为"BPBall", 并在蓝图里添加一个有物理系统的球体(Sphere)
    * 添加组件 球体
    * 更换 Material 材质
    * 添加 Camera 摄像机 与 Spring Arm 弹簧臂组件, 用来跟随玩家角色
    * 弹簧臂组件取消继承 Pitch, Yaw, Roll
    * 勾选 Simulate Physics 模拟物理
    * 勾选 Gravity 重力
    * 设置 Linear Damping 线性阻尼 / Angular Damping 角阻尼
    * 设置 MassInKg 质量(千克)

    ![输入图片说明](https://images.gitee.com/uploads/images/2020/1020/235839_bd1835c0_792465.png "微信图片_20201020235829.png")

  * 创建一个GameMode, "RollingGameMode".
    * 在 World Settings -> Game Mode 添加一个新的 Game Mode
    
    ![创建一个新的GameMode](https://images.gitee.com/uploads/images/2020/1021/000005_5b57fd2f_792465.png "微信图片_20201020235939.png")

  * 将Default Pawn选择成"BPBall"
  * Mouse Input
    * 添加事件 Mouse X - 鼠标的左右移动
    * 添加事件 Mouse Y - 鼠标的前后移动
    * 了解：Left Button 鼠标左键 / Right Button 鼠标右键 / Wheel 鼠标滚筒
    * 了解：Make Vector 创建向量
    * 了解：Add Torque 添加扭矩

  * Keyboard Input 
    * 添加事件 Space
    * 了解：Ctrl / Shift / Command / Alt
    * 了解：A~Z
    * 了解：Set Velocity (设置物理线性速度)
    * 了解：Launch (发射)

   ![输入图片说明](https://images.gitee.com/uploads/images/2020/1021/000220_079b2eb5_792465.png "微信图片_20201021000207.png")
 
* ### 创建一个秒表
  * Text Render
  * Event BeginPlay (开始时只运行一次)
  * Event Tick (运行过程中不断执行)
  * 变量 (Float, Integer, String, Boolean, Vector)
  * Delay

  ![输入图片说明](https://images.gitee.com/uploads/images/2020/1021/000401_24d21dd6_792465.png "微信图片_20201021000345.png")

* ### Random 随机
  * 变动IoTLight的位置
  * 为创建随机城市做准备

<br>

--------------------------
### <i>作业：球球大冒险</i>
- 使用StarterContent
- 创建一些比较难通过的地形
- 创建一个可以鼠标控制的球(Pawn)
- 创建可以触发变色的灯光(Actor)
- 创建一个计时器
--------------------------
<br>

## 5. 使用 Unreal Engine Market 的内容丰富你的场景
* 复制Content里的内容
* Megascans Abandoned Apartme
* Low Poly Rainforest
* Low Poly Tropical
* Affordable Landscapes 2 (AL1)

## 6. 开场动画 Cinematic
* Level Sequence
* Master Sequence

## 7. 小心，你闯入了禁入森林
* 高度雾 Fog
* 体积光 Volumetric Light
* 环境声音 Ambient Sound
* 声音空间化 Sound 
* 全局后期处理 Global Post Processing Volume
* 后期处理体积 Post Processing Volume

## 8. 为球球添加各种技能
* 超级跳
    * Do Once
    * Do N
* 超级冲刺
    * 获取物理线性速度
    * 设置物理线性速度
* 变色
    * FlipFlop
* 变身
    * 设置静态网格体
* 放大缩小
    * Branch
* 瞬移门
    * 设置位置
* 火焰
    * Spawn

## 9. 为场景添加特殊物件
* 隐形的墙
    * 阻挡体积
    * Text Render
* 一个不停旋转的障碍物
    * 创建旋转体
    * 设置旋转
    * Timeline
        * 浮点型 Float
        * 使用最后一帧
        * 循环
* 一个巡逻的球
    * Timeline
        * Vector
* 摆动的阻挡地块
    * Timeline
        * Vector
* 掉入深渊就返回原地
* 胜利区域

## 10. 为游戏添加UI
* 添加血量和魔法量
    * 为 Ball 添加公有变量 HP（血量） 和 MP（魔法值） 
    * 为 Ball 添加公有变量 MaxHP 和 MaxMP
* 技能按钮
* 添加暂停菜单
    * LOGO
    * 返回游戏按钮
    * 退出游戏按钮

## 11. 优化场景

* 剔除距离体积
    
    ![输入图片说明](https://docs.unrealengine.com/Images/Engine/Rendering/VisibilityCulling/CullDistanceVolume/ExampleScene_SuggestedPairValues.webp "")

* 优化载入
    * Level Streaming Volume

* 优化光照
    * Lightmass Importance Volume
    * LightmassCharacterIndirectDetailVolume1

## 流程控制
* Branch
* FlipFlop
* Do Once
* Do N
* DoOnce_MultiInput
* ForLoop
* Gate
* MultiGate
* Squence与Delay

## UI
* Widget

## Materials 材质

## Animation 动画
* 纸上2D游戏
* 骨架
* 骨骼模型（Skeletal Mesh）
* 动画序列（Animation Sequence）
* 顶点动画

## 使用Random创建一座城

## Paper2D

## 粒子系统

## Audio
