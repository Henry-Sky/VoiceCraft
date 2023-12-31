# 语音信号特点

**声波分类**
- 振动: 纵波
- 频率: 听觉范围内的声波、超声波、次声波
- 形状: 连续波、脉冲波
- 幅度: 平面波、衰减波


**清音和浊音**
- 清音:

- 浊音:
    - 特点: 周期性震动
    - 属性: 基音频率, 基音周期



# 语音信号采集

**采样与量化**
- 前提假设: (短时平稳假设),语音信号在10~30ms时间内是平稳的
- 过程: 模拟信号转数字信号
- 方法: 假设语音信号 Xa(t) 表示振幅值随着连续变量t的变化趋势, 以一定时间间隔T对这样的连续信号取值



# 语言信号处理
## 时域分析
语音信号的主要时域特征  
窗函数  
共振频率、共振峰  
短时平局幅度、短时平均过零率  

## 频域分析

## 信号处理

**<font color=red>动态时间规整(DTW)</font>**
- 用途: 衡量两个长度不同的时间序列的相似度
- 原理: DTW算法通过局部优化的方法实现加权距离总和最小
- 路径优化方法: 局部约束, 全局约束, 动态规划


## 通用处理
语音信号端点检测的方法



# 语言识别

汉语中音素的构成  
最小发声单位：音素

**<font color=red>统计分词法</font>**
- 模型:
    1. 隐马尔可夫模型
    2. 最大熵模型
    3. 条件随机场
    4. N-gram模型
- 原理: 



# 说话人识别

**混合高斯模型(GMM)**
- 定义: 由 K 个单高斯模型组合而成的模型,这 K 个子模型是混合模型的隐变量,故混合高斯模型又称多维概率密度函数
- 前提: 对每个说话人进行采样训练
- 原理: 为每个目标说话人语音建立一个GMM模型,根据不同的应用评估得分
- 缺点: 无法判断非采样说话人的声音

**<font color=red>通用背景模型(UBM)</font>**
- 特点: UBM取一个与说话人无关的模型作为集外说话人模型
- 原理: 用很多不同说话人在各种环境下的语音数据训练获得
- 特性: 是所有说话人语音特征共性的反映及环境通道的共性反应
- 优点: 可以判断是否集外人(非采样说话人)

反映说话人个性化特征的参数
- 辨别性: 具有很高的区别说话人的能力
- 顽键性: 不易在输入语音受到传输通道和噪声的影响
- 独立性: 特征的各维参数之间应该具有独立性
- 简洁: 易于提取, 计算, 不易被模仿

基于SVM说话人模型
- 一对一: 每个说话人, 每个冒认者训练
- 一对多: 每个说话人和所有冒认者一起训练

影响语音识别的环境因素有哪些
1. 加性噪声
2. 通道畸变
3. 人为因素
4. 瞬间噪声
5. 来自其他话者的干扰