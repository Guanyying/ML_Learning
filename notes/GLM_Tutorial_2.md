# 广义线性模型

## 从指数分布族引出广义线性模型

通过对[指数分布族](./GLM_Tutorial_1.md)的回顾，观察伯努利分布的指数分布族形式中的$\eta$:
$$\eta = \log{\frac{\phi}{1-\phi}}$$
则：
$$\frac{\phi}{1-\phi} = \rm{exp}(\eta)$$
$$\phi = (1-\phi)\rm{e}^{\eta}$$
$$\phi = \frac{\rm{e}^{\eta}}{1+\rm{e}^{\eta}}=\frac{1}{1+\rm{e}^{-\eta}}$$
**上式恰好是logistic函数！**

再来观察高斯分布的指数分布族形式中的$\eta$:
$$\eta = \frac{\mu}{\sigma^2}$$
则：
$$\mu = \sigma^2\eta$$
**上式恰好是线性函数！**

**归纳：**  
1. 伯努利分布的参数$\phi$，与$\eta$的映射函数是logistic函数，**对应逻辑回归模型**。
2. 高斯分布的参数$\mu$，与$\eta$的映射函数是线性函数，**对应线性回归模型**。

**总结：**  
1. $\eta$以不同的映射函数与其它概率分布函数中的参数发生联系，从而得到不同的模型。
2. 广义线性模型正是将指数分布族中的所有成员（每个成员正好有一个这样的联系）都作为线性模型的扩展，通过各种非线性的连接函数将线性函数映射到其他空间，从而大大扩大了线性模型可解决的问题。

## 广义线性模型的形式化定义
1. 给定样本$\mathbf{x}$与模型参数$\theta$，样本分类$y$服从指数分布族中的某个分布，记为：
$$p(y|\mathbf{x};\theta): \rm{Exponential Family}(\eta)$$
2. 给定$\mathbf{x}$，我们需要的目标函数为：
$$h_{\theta}(x) = E[T(y)|x]$$
3. $$\eta = \theta^Tx$$

## 根据GLM形式化定义推导logistic模型

## 根据GLM形式化定义推导线性回归模型