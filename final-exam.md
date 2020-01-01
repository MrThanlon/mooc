# 1.

设$X_i=\{击中的导弹个数为i\},i=0,1,2,3$

$B={坠毁}$

由全概率公式，$P(B)=\sum\limits_{i=0}^3P(B|X_i)P(X_i)=0.444$

# 2.

$X$的分布函数
$$
F_X(x)=\int_{-\infin}^{+\infin}f(x)dx=
\begin{equation}
\begin{cases}
1-e^{-x},x>0\\
0,x\le0
\end{cases}
\end{equation}
$$
由$Y=3X+1$，所以$X=\frac{Y-1}{3}$，得$Y$的分布函数
$$
F_Y(y)=
\begin{equation}
\begin{cases}
1-e^{-\frac{y-1}{3}},y>1\\
0,y\le1
\end{cases}
\end{equation}
$$
故$Y$的概率密度函数
$$
f_Y(y)=F_Y'(y)=
\begin{equation}
\begin{cases}
\frac{1}{3}e^{-\frac{y-1}{3}},y>1\\
0,y\le1
\end{cases}
\end{equation}
$$

# 3.

由题意，有
$$
\int_{-\infin}^{+\infin}\int_{-\infin}^{+\infin}f(x,y)dxdy=
\int_{0}^1dx\int_0^xcxydy=
\frac{c}{8}=1
$$
故$c=8$

计算边缘概率密度函数
$$
f_X(x)=\int_{-\infin}^{+\infin}f(x,y)dy=
\begin{equation}
\begin{cases}
4x^3,0<x<1\\
0,others
\end{cases}
\end{equation}
$$

$$
f_Y(y)=\int_{-\infin}^{+\infin}f(x,y)dx=
\begin{equation}
\begin{cases}
4y,0<y<1\\
0,others
\end{cases}
\end{equation}
$$

显然，$f(x,y)\neq f_X(x)f_Y(y)$，故$X$与$Y$不相互独立。

# 4.

因为$X$与$Y$相互独立，所以有
$$
E(X+Y)=E(X)+E(Y)=\lambda+\lambda^{-1}
$$

$$
D(X+Y)=D(X)+D(Y)=\lambda+\lambda^{-2}
$$

# 5.

构造似然函数
$$
L(\theta)=\theta^n\prod_{i=1}^nx_i^{\theta-1}
$$

$$
\ln L=n\ln\theta+(\theta-1)\sum_{i=1}^{n}\ln x_i
$$

$$
\frac{\partial\ln L}{\partial\theta}=
\frac{n}{\theta}+\sum_{i=1}^{n}\ln x_i=0
$$

则$\theta$的极大似然估计$\hat\theta=-\frac{n}{\sum\limits_{i=1}^{n}\ln x_i}$

# 6.

由题意，构造检验假设$H_0:\mu=140,H_1:\mu\neq 140$

令
$$
T=\frac{\overline{X}-\mu}{\frac{S}{\sqrt{n}}}\sim t(24)
$$
则$H_0$的拒绝域：$\{T||T|>t_{0.025}(24)\}$

当$H_0$成立时，$T=\frac{155-140}{\frac{25}{\sqrt{25}}}=3>t_{0.025}(24)=2.0639$

故拒绝原假设，即认为高原地区成年男子的血红蛋白不正常。

# 7.

$$
R=\frac{l_{xy}}{\sqrt{l_{xx}l_{yy}}}=0.943>R_{0.05}(10)=0.576
$$

所以认为家庭收入和食品支出存在显著的线性相关关系。
$$
\hat{b}=\frac{l_{xy}}{l_{xx}}=0.204\\
\hat{a}=\overline{y}-\hat{b}\overline{x}=2.368
$$
线性回归方程为 $\hat{y}=0.204x+2.368$