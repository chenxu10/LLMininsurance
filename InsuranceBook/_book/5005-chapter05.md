# 赢了概率,输了赌局

如果把每一笔交易都当成一场战争，那么在投入到血雨腥风之前，
我们必须先算好自己的获胜概率与下注的金额(dosage or betting ratio)，否则就容易赢了概率输了赌局。
但如果我们的下注比例调整准确则可以如爱德华.索普(Edward Thorp)说的那样用庄家的钱赚钱。
曹操批孙子兵法有云：“故战必先算其费，因粮于敌也。”
1992年，爱德华.索普与Louis Rotando联合发表了凯利判据(Kelly Criterion)是如何应用于股票市场的资源分配问题的。

### 凯利判据的核心思想
假设你有一笔初始资金，你和庄家对赌，庄家拥有远大于你的接近无限的本金，但是设你用演绎法获得了一些信息优势。
每次赌局，你获胜的概率是0.7，而庄家获胜的概率是0.3。现在问你每笔赌局你应该下注多少，才能最大化你的收益，同时避免赌徒毁灭的困局。

爱德华.索普创造性地调整了优化的指标，既不是最小化毁灭的概率E(x0->0)，而不是最大化收益E(xn),而是最大化资本增长率对数转化下的几何平均
而非算术平均即E(log(xn/x0)^1/n)。如果我们要使得该值最大，那么每次下注的比例就是b - q/p，其中b是你潜在的获利除以你需要付出的成本，
p是你获胜的概率，q是你输的概率。

### 凯利判据与等加速运动和信息论类比
如果从信息论的视角去观察凯利希望最优化的增长率指数公式我们会发现它与香农信息熵公式的构造有惊人的相似。
香农信息熵公式为H(x) = -∑p(x)log(p(x))。香农信息熵提出的背景是在一个数据通信系统中，
假如我们有信息源，有通信渠道和接受者，如果一个系统完全没有背景噪音，那么信号可能丢失或损失，假如噪音太大
信号的传导不是最优的，所以我们需要找到一个合适的平衡点。

如果从物理运动视角去观察凯利判据，我们以下注的比例f为x轴，G(f)对数几何平均增长率为y轴，
我们会发现它与物理等加速运动的轨迹有惊人的相似。一旦下注比例超过了最优值，dy/dt速度就会变成负数。

### 凯利判据 vs 现代投资组合理论
现代投资理论假设资产的收益率服从正态分布，并且对基于历史数据的协方差矩阵的参数估计准确性要求很高。
它假设你对所有资产的联合概率分布有一个很好的估计，但是在实际中，我们很难得到这样的估计。相反，如果我们
在实践中使用凯利判据，我们要做的是不断根据最坏情况和期望收益的比例动态调整我们的下注比例，在投资组合的配比领域，
凯利判据相比于现代投资组合理论或许有更好的抗模型风险能力。如我们在第二篇文章讨论的，模型风险与风险模型
是两个截然不同但是容易混淆的概念。
 
## 推荐书目与核心概念
1. Thorp, E. O. (2008). The Kelly criterion in blackjack sports betting, and the stock market. In Handbook of asset and liability management (pp. 385-428). North-Holland.
2. Shannon, C. E. (1948). A mathematical theory of communication. The Bell system technical journal, 27(3), 379-423.
