一个普通的乙线性常微分方程$y' = f(x,y)$从$(x_0,y_0)$开始的初值问题的解，并且$f(x,y)$连续且满足Lipschitz条件，满足：
$$
f(x) = y_0 + \int_{x_0}^xf(t,f(t))dt
$$
所以这是一个不动点问题，是对映射$\phi$：
$$
\phi:f\rightarrow y_0+\int_{x_0}^x f(t,f(t))dt
$$
在Banach空间（因为我们预设$f(x,y)$是连续的）上的不动点。

如果这个映射是一个收缩映射，由于Banach不动点定理，任取一个$f$，被$\phi$作用许多次，就能找到它的不动点（而且Banach不动点定理还保证了不动点的存在和唯一，这和度量空间的完备性有关）。

为了证明（另）这是一个收缩映射，用到了它满足的Lipschitz条件：
$$
\begin{align}
d(\phi(f_1),\phi(f_2)) & =  min(\phi(f_1) - \phi(f_2)) \\
&=min(\int_{x_0}^x\{f_1(t, f_1(t)) -f_2(t,f_2(t))\}dt)\\
&\leq min(\int_{x_0}^xK(f_1(t)-f_2(t)))dt\\
&\leq K\alpha min(f_1 - f_2)\\
&=K\alpha d(f_1,f_2)
\end{align}
$$
这样，只需要有$\alpha < \frac {1}{K}$就有它是一个收缩映射，从而通过Banach不动点定理保证了解的存在唯一性。