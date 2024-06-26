也即三极管
# 结构及类型
## 构成方式
![[双极型晶体管BJT.png]]
![[双极型晶体管BJT-1.png]]
### 三个区域
#### 发射区
发射载流子的区域
掺杂浓度最高，需要有丰富的载流子
#### 集电区
收集载流子的区域
掺杂浓度不高，面积大
类比仓库，要收集东西，需要剩余空间大
#### 基区
掺杂浓度低，非常薄
### 三个电极

### 两个结
发射结，集电结
箭头指向发射结导通的方向（从正到负）
# 电流放大作用

## 放大
==放大的基本要求：不能失真==
三级管中的集电极与基极有
$$
i_{c}=\beta i_{b}
$$
## 基本共射放大电路
![[双极型晶体管BJT-2.png|400]]
工作时：
发射结正偏，集电结反偏
### 内部载流子的运动
![[双极型晶体管BJT-3.png|400]]
#### 发射结正偏
扩散运动恢复，大量自由电子向基区扩散，基区中的空穴向发射结扩散
形成两个电流：
$I_{EP}$和$I_{EN}$，但是$I_{EN}\gg I_{EP}$
#### 基区
基区薄且掺杂浓度低，那么由发射区到基区的自由电子大部分不会与空穴复合
在空穴与电子复合后$I_{B}$会源源不断产生空穴，显然产生的速度与总电流是成比例的。
#### 集电结收集自由电子
反偏时存在一漂移电流$I_{CBO}$很小，可以忽略

反偏时，集电结有很大的指向基区的电场，不断吸引基区中的自由电子。

### $\beta$放大系数
$$
\bar{\beta}=\frac{\bar{I}_{CN}}{\bar{I}_{BN}}=\frac{I_{C}-I_{CBO}}{I_{B}+I_{CBO}}\approx \frac{I_{C}}{I_{B}}
$$
共射交流电流放大系数：
$$
\beta=\frac{\Delta I_{C}}{\Delta I_{B}}
$$
在绝大多数情况下，而这数值很接近
### $I_{CEO}$穿透电流
当$I_{B}=0$时，$C到E$的电流
### $I_{CBO}$
### $\alpha$共基放大系数
$$
\bar{\alpha}\approx \frac{I_{C}}{I_{E}}=\frac{\bar{\beta}}{1+\bar{\beta}}
$$
## BJT共射特性曲线
### 输入特性
$$
i_{B}=f(U_{BE})|_{U_{CE}=Const}
$$
![[双极型晶体管BJT-8.png|300]]
两个特点： $U_{CE}$越小，越往左移动，但是当$U_{CE}$超过某个阈值时，曲线不再右移
这与集电结作用有关：
当$U_{CE}$很小时，集电结内部反偏程度不高，收集电子能力较差
当$U_{CE}$升高时，集电结收集电子能力提高，减少了基区内部电子复合的机会，从而导致同样的$U_{BE}$作用下$i_{B}$减小。
当$U_{CE}$超过$1V$时，集电结收集电子能力已经很强，发射区到基区的电子基本都被集电极收集，以至于$U_{CE}$再增加也不会导致$I_{B}$减小。
### 输出特性
$$
i_{C}=f(U_{CE})|_{I_{B}=const}
$$
![[双极型晶体管BJT-7.png|400]]
$I_{B}=0$时，仍有一个电流，为穿透电流$I_{CBO}$
#### 放大区
发射极正偏，集电结反偏，$i_{B},i_{C}$成比例
#### 截止区
两个结都反偏，$C,E$断路
只需基极电位小于发射极电位即位于截止区
#### 饱和区
双结正偏
$U_{CES}$类似于$C,E$间开关闭合
这时
$\beta I_{B}>I_{Cmax}$
## 三极管的主要参数
### 极限参数
从略
### 温度的影响
温度对输入特性的影响：
![[双极型晶体管BJT-9.png|350]]
温度升高，曲线左移
温度升高，会使发射结的正向压降降低，每升高1°C，$U_{BE}$减小1.9~2.5mV
对输出特性：
![[双极型晶体管BJT-10.png|400]]
温度升高，$\beta$增大
## 光电三极管
基极换为光感材料，作为光电传感器。
可用于光电耦合器，使用一发光二极管控制电流，从而实现两侧完全电气绝缘。
也可配合光纤实现电信号转光信号传递。