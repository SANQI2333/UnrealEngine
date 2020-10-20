# UE4 课程

## 1.	关卡设计师入门

打开 /Content/StarterContent/Maps/StarterMap

* 了解：Actor, Pawn, Character, Static Mesh.
* 了解：ThirdPerson, FirstPerson, 
* 了解：Directional Light（定向光源）, Point Light（点光）, Spot Light（聚光）, Sky Light（天光）
* 了解：静态光照，Static Lighting Level Scale，Num Indirect Lighting Bounces
* 了解：Lightmass Importance Volume
* 了解：Post Processing Volume

https://docs.unrealengine.com/zh-CN/Engine/QuickStart/index.html


## 2.	蓝图的Hello World

* 了解：BoxTrigger, Events
* 了解：Print
* 了解：数据类型string
* 了解：关卡蓝图
* 了解：Actor蓝图

<br>

--------------------------
### 作业：灭火人
- 使用StarterContent
- 创建一块地
- 创建一些触碰就会熄灭的火球
--------------------------
<br>

## 3.	使用蓝图控制

创建一个新“空工程”，来做一个滚动的球

* ### 创建一个灯光控制 (Actor)
  * 回忆：Box Collision
  * 创建一个地板按钮
  * 控制灯光开关
    * 了解：注释
    * 了解：branch(if)
    * 了解：Boolean
  * 控制灯光颜色

* ### 创建一个玩家可以控制的滚动的球 (Pawn)
  * 创建一个Pawn蓝图, 并在蓝图里创建一个有物理系统的球体(Sphere)
    * 了解：Material 材质
    * 了解：Simulate Physics 模拟物理
    * 了解：Gravity 重力
    * 了解：Linear Damping 线性阻尼 / Angular Damping 角阻尼
    * 了解：MassInKg 质量(千克)

    ![输入图片说明](https://images.gitee.com/uploads/images/2020/1020/235839_bd1835c0_792465.png "微信图片_20201020235829.png")

  * 创建一个GameMode, "RollingGameMode".
    * 了解：World Settings -> Game Mode
  * Mouse Input
    * Mouse X
    * Mouse Y
    * Left Button / Right Button / Wheel
    * 了解：Make Vector (3D向量)
    * 了解：Add Torque (扭矩)
  * Keyboard Input 
    * Space
    * Ctrl / Shift / Command / Alt
    * A~Z
    * 了解：Set Velocity (速度)
    * 了解：Launch (发射)
 
* ### 创建一个秒表
  * Text Render
  * Event BeginPlay (开始时只运行一次)
  * Event Tick (运行过程中不断执行)
  * 变量 (Float, Integer, String, Boolean, Vector)
  * Delay

* ### Random 随机
  * 变动IoTLight的位置
  * 为创建随机城市做准备

<br>

--------------------------
### 作业：球球大冒险
- 使用StarterContent
- 创建一些比较难通过的地形
- 创建一个可以鼠标控制的球(Pawn)
- 创建可以触发变色的灯光(Actor)
- 创建一个计时器
--------------------------
<br>


## 4.	使用Random创建一座城

--------------------------

## 5.	使用Packs丰富场景
了解：目录结构

--------------------------

## Landscape and Foliage地形与植物

## Post Processing 后期处理

## Cinematic 过场动画

## Paper2D

## UI

## 粒子系统

## Materials

## Animation

## Audio
