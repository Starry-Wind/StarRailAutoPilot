# StarRailAutoPilot
基于小地图寻路的锄大地脚本

由于是非常早期的开发版本，目前需要先移动到对应的地图，StarRailAutoPilot.py中设置好路线编号，并在起始点开启脚本。

## 功能列表
- 定位坐标 已经完成
- 开拓模式（根据路线图寻路）：基本完成
- 巡猎模式（小地图遇敌时，根据敌人位置进行攻击）：目前还没加战斗判定
- 主角模式（将可破坏物也一并收集）：暂时没实现，应该添加一种新的标点就可以了
- 自动寻路：基于jps以及Astar算法自动寻找点位，目前效果不如绘制的路线

## 如何绘制路线图

maps文件夹中存储了地图的原图以及路线图(xx-x.png)。复制一份原图，在图上直接画点，不同RGB颜色代表不同的点，目前只有两种：
1. 起始点（青色[0,255,255]），一般标在传送点附近
2. 普通导航点（黄色[255,255,0]）


目前暂时是根据离当前点最近的点作为下一个点，所以标点的时候要注意尽量不要出现锐角。后续可能会使用颜色的饱和度或者亮度作为先后排序依据。
后续可能会加入：入画点、电梯操作点等特殊操作点位

## 相关项目

- JPS寻路 https://github.com/ViktorRubenko/Jump-Point-Search
- 自动锄大地 https://github.com/Starry-Wind/StarRailAssistant
- 自动模拟宇宙 https://github.com/CHNZYX/Auto_Simulated_Universe
