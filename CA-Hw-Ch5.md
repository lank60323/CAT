# CA-Hw-Ch5

**4.** 求下列积分：

(2) $\displaystyle\int_0^{2\pi}\frac{r-\cos\theta}{1-2r\cos\theta+r^2}\,\mathrm{d}\theta$；

$\textbf{sol:}$
(2)$I = \oint_{|z| = 1} \frac{r - \frac{z + z^{-1}}2}{1 - 2r \frac{z + z^{-1}}2 + r^2}\frac{dz}{iz} = \oint_{|z| = 1}\frac{2rz - z^2 - 1}{2i(z - r)(1 - rz)z}dz$
因此 $z = r,z = \frac 1r , z = 0$ 是一级极点
其留数分别为
$$\operatorname{Res}[f,r] = \frac{i}{2r},\quad \operatorname{Res}[f,\frac 1r] = -\frac i{2r},\quad \operatorname{Res}[f,0] = -\frac i{2r} $$
①当 $|r| < 1$ 时，$I = 2\pi i \cdot(\operatorname{Res}[f,r] + \operatorname{Res}[f,0]) = 0$
②当 $|r| > 1$ 时，$I = 2\pi i \cdot (\operatorname{Res}[f,\frac 1r] + \operatorname{Res}[f,0]) = \frac{2\pi}r$
③当 $r = 1$ 时，$I = \oint_{|z| = 1} \frac 1{2iz}dz = \pi$
④当 $r = -1$ 时，$I = \oint_{|z | = 1} -\frac 1{2iz}dz = -\pi$
(3) $\displaystyle\int_0^{\frac{\pi}{2}}\frac{\mathrm{d}\theta}{a^2+\sin^2\theta}\ (a>0)$。

$\textbf{sol:}$
$I = \frac 12 \oint_{|z| = 1} \frac {2i}{z^2 - (4a^2 + 2)z + 1}dz$
由求根公式可得
$z_{1,2} = (2a^2 + 1) \mp 2a\sqrt{a^2 + 1}$
则 $z_1 < 1,z_2 > 1$ 因此在单位圆里的级数是 $z_1$ 
则 $\operatorname{Res}[f,z_1] = -\frac{2i}{4a\sqrt{a^2 + 1}}$ 
因此 $I = \frac 12 \cdot 2\pi i \sum_{|z_k| < 1} \operatorname{Res} = \frac \pi{2a\sqrt{a^2 + 1}}$


**5.** 求下列积分：

(1) $\displaystyle\int_{-\infty}^{+\infty}\frac{x^2}{(x^2+a^2)^2}\,\mathrm{d}x\ (a>0)$；

$\textbf{sol:}$
由于 $\deg(x^2+ a^2)^2 = 4 = \deg (x^2) + 2$ 且 $(x^2 + a^2)^2$ 在实轴上无零点
所以有 $I = 2\pi i \sum_{\operatorname{Im}x_k > 0}\operatorname{Res}[f,x_k]$
其中
$f = \frac {x^2}{(x - ai)^2(x + ai)^2}$ 因此在上半部分的极点为 $ai$ 
易由留数公式得出 $\operatorname{Res}[f,ai] = \lim_{x \rightarrow ai}\frac d{dx}[(x - ai)^2\cdot f] = \frac 1{4ai}$
因此$I = 2\pi i \cdot \operatorname{Res}[f,ai] = \frac{\pi}{2a}$


(3) $\displaystyle\int_0^{+\infty}\frac{1+x^2}{1+x^4}\,\mathrm{d}x$。

$\textbf{sol:}$
由于 $\deg(1 + x^4) = 4 = \deg (1 + x^2) + 2$ 且 $1 + x^4$ 在实轴上无零点
所以有 $I = \frac 12\int_{-\infty}^{+\infty}\frac{1+x^2}{1+x^4}\,\mathrm{d}x = \pi i \sum_{\operatorname{Im}x_k > 0}\operatorname{Res}[f,x_k]$
其中由 $1 + x^4 = 0$ 可得在上半平面的极点是 $x = e^{i\frac \pi 4},e^{i\frac {3\pi}4}$
易得 $\operatorname{Res}[f,e^{i\frac \pi 4} ] = -\frac 14(e^{i\frac \pi 4} + e^{i\frac {3\pi}4}) = -\frac {\sqrt{2}}4 i$ 
$\operatorname{Res}[f,e^{i\frac{3\pi}4}] = -\frac 14(e^{i\frac \pi 4} + e^{i\frac {3\pi}4}) = -\frac {\sqrt{2}}4 i$
所以 $I = \pi i \cdot 2(-\frac{\sqrt{2}}4 i) = \sqrt{2}\pi/2$  


**6.** 求下列积分：

(1) $\displaystyle\int_0^{+\infty}\frac{x\sin ax}{x^2+b^2}\,\mathrm{d}x\ (a>0,\ b>0)$；

$\textbf{sol:}$
由于 $\frac{x\sin ax}{x^2+b^2}$ 为偶函数
所以 $\mathrm{I} = \frac 12 \int_{-\infty}^{+\infty}\frac{x\sin ax}{x^2+b^2}\,\mathrm{d}x$
考虑 $\mathrm{I}' = \frac 12 \int_{-\infty}^{+\infty}\frac{x\,\mathrm{e}^{\mathrm{i}ax}}{x^2+b^2}\,\mathrm{d}x$ ，$\mathrm{I}$ 即是 $\mathrm{I}'$ 取虚部
由于 $\deg(x^2 + b^2) = 2 = \deg(x\sin ax) + 1$ 且 $x^2 + b^2$ 在实轴上无零点
则有 $\mathrm{I}' = \pi \mathrm{i} \sum_{\operatorname{Im} z_k > 0}\operatorname{Res}[\frac z{z^2 + b^2} \mathrm{e}^{\mathrm{i}az},z_k]$
易知在上半平面的极点只有 $z = bi$，且其为一级极点
得到 $\operatorname{Res}[\frac z{z^2 + b^2}\mathrm{e}^{\mathrm{i}az},b\mathrm{i}] = \frac 1{2\mathrm{e}^{ab}}$
因此 $\mathrm{I}' = \frac \pi{2\mathrm{e}^{ab}}\mathrm{i}$ ，取其虚部便得 $\mathrm{I} = \frac\pi{2\mathrm{e}^{ab}}$.


(2) $\displaystyle\int_0^{+\infty}\frac{\sin ax}{x(x^2+b^2)}\,\mathrm{d}x\ (a>0,\ b>0)$；

$\textbf{sol:}$
由于 $\frac{\sin ax}{x(x^2 + b^2)}$ 是偶函数
因此 $\mathrm{I} = \frac 12\int_{-\infty}^{+\infty} \frac{\sin ax}{x(x^2+b^2)}\,\mathrm{d}x$
考虑 $\mathrm{I}' = \frac 12 \int_{-\infty}^{+\infty}\frac{\mathrm{e}^{\mathrm{i}ax}}{x(x^2+b^2)}\,\mathrm{d}x$ ，$\mathrm{I}$ 即是 $\mathrm{I}'$ 取虚部
由于 $\deg(x(x^2 + b^2)) > 1$ 且 $x(x^2 + b^2)$ 在实轴上有零点 $x = 0$
则有 $\mathrm{I}' = \pi \mathrm{i} \sum_{\operatorname{Im} z_k > 0}\operatorname{Res}[\frac 1{z(z^2 + b^2)} \mathrm{e}^{\mathrm{i}az},z_k] + \frac 12 \pi \mathrm{i}\sum_{\operatorname{Im}z = 0} \operatorname{Res}$
易知在上半平面的极点只有 $z = bi$，且其为一级极点
得到 $\operatorname{Res}[\frac 1{z(z^2 + b^2)} \mathrm{e}^{\mathrm{i}az},z_k] = -\frac 1{2b^2\mathrm{e}^{ab}},\quad \operatorname{Res}[\frac 1{z(z^2 + b^2)} \mathrm{e}^{\mathrm{i}az},0] = \frac 1{b^2}$
因此 $\mathrm{I}' = \frac \pi{2b^2}(1 - \frac 1{\mathrm{e}^{ab}})\mathrm{i}$ ，取其虚部得到 $\mathrm{I} = \frac \pi{2b^2}(1 - \frac 1{\mathrm{e}^{ab}})$


(3) $\displaystyle\int_0^{+\infty}\frac{x^2-a^2}{x^2+a^2}\,\frac{\sin x}{x}\,\mathrm{d}x\ (a>0)$；

$\textbf{sol:}$
由于 $f = \frac {x^2 - a^2}{x^2 + a^2} \cdot \frac {\sin x}x$ 为偶函数
所以 $\mathrm{I}  = \frac 12\int_{-\infty}^{+\infty}\frac{x^2-a^2}{x^2+a^2}\,\frac{\sin x}{x}\,\mathrm{d}x$
考虑 $\mathrm{I}' = \frac 12\int_{-\infty}^{+\infty} \frac{x^2 - a^2}{x(x^2 + a^2)} \mathrm{e}^{\mathrm{i}x}\,\mathrm{d}x$ ，$\mathrm{I}$ 即是 $\mathrm{I}'$ 取虚部
由于 $\deg(x(x^2 + a^2)) = 3 = \deg(x^2 - a^2) + 1$ 且 $x(x^2 + a^2)$ 在实轴上有零点 $x = 0$
则有 $\mathrm{I}' = \pi \mathrm{i} \sum_{\operatorname{Im} z_k > 0}\operatorname{Res}[\frac{z^2 - a^2}{z(z^2 + a^2)} \mathrm{e}^{\mathrm{i}z},z_k] + \frac 12 \pi \mathrm{i}\sum_{\operatorname{Im}z = 0} \operatorname{Res}$
易知在上半平面的极点只有 $z = a\mathrm{i}$，且其为一级极点
得到 $\operatorname{Res}[\frac{z^2 - a^2}{z(z^2 + a^2)} \mathrm{e}^{\mathrm{i}z},a\mathrm{i}] = \frac{-2a^2}{a\mathrm{i}\cdot 2a\mathrm{i}}\mathrm{e}^{-a} = \frac 1{\mathrm{e}^{a}},\quad \operatorname{Res}[\frac{z^2 - a^2}{z(z^2 + a^2)} \mathrm{e}^{\mathrm{i}z},0] = \frac{-a^2}{a^2} = -1$
因此 $\mathrm{I}' = \pi(\frac 1{\mathrm{e}^a} - \frac 12)\mathrm{i}$ ，取其虚部得到 $\mathrm{I} = \pi(\frac 1{\mathrm{e}^a} - \frac 12)$


(4) $\displaystyle\int_0^{+\infty}\frac{\cos 2ax-\cos 2bx}{x^2}\,\mathrm{d}x\ (a>0,\ b>0)$；

$\textbf{sol:}$
由于 $\frac{\cos 2ax - \cos 2bx}{x^2}$ 为偶函数
所以 $\mathrm{I} = \frac 12\int_{-\infty}^{+\infty}\frac{\cos 2ax-\cos 2bx}{x^2}\,\mathrm{d}x$
考虑 $\mathrm{I}' = \frac 12\int_{-\infty}^{+\infty}\frac{\mathrm{e}^{2\mathrm{i}ax} - \mathrm{e}^{2\mathrm{i}bx}}{x^2}\,\mathrm{d}x$ ，$\mathrm{I}$ 即是 $\mathrm{I}'$ 取实部
由于 $\deg(x^2) = 2 \geq 0 + 1$ 且 $x^2$ 在实轴上有零点 $x = 0$
又 $z = 0$ 是 $\mathrm{e}^{2\mathrm{i}az} - \mathrm{e}^{2\mathrm{i}bz}$ 的一级零点，所以 $z = 0$ 是 $\frac{\mathrm{e}^{2\mathrm{i}az} - \mathrm{e}^{2\mathrm{i}bz}}{z^2}$ 的一级极点，且上半平面无极点
则有 $\mathrm{I}' = \frac 12 \pi \mathrm{i}\sum_{\operatorname{Im}z = 0} \operatorname{Res}$
得到 $\operatorname{Res}[\frac{\mathrm{e}^{2\mathrm{i}az} - \mathrm{e}^{2\mathrm{i}bz}}{z^2},0] = \lim_{z \rightarrow 0}\frac{\mathrm{e}^{2\mathrm{i}az} - \mathrm{e}^{2\mathrm{i}bz}}{z} = 2(a - b)\mathrm{i}$
因此 $\mathrm{I}' = \frac 12\pi\mathrm{i}\cdot 2(a - b)\mathrm{i} = \pi(b - a)$ ，取其实部得到 $\mathrm{I} = \pi(b - a)$


(5) $\displaystyle\int_0^{+\infty}\left(\frac{\sin x}{x}\right)^3\mathrm{d}x$。

［提示：取 $f(z)=\dfrac{\mathrm{e}^{3\mathrm{i}z}-3\mathrm{e}^{\mathrm{i}z}+2}{z^3}$。］

$\textbf{sol:}$
由于 $(\frac{\sin x}x)^3$ 为偶函数
所以 $\mathrm{I} = \frac 12\int_{-\infty}^{+\infty}(\frac{\sin x}x)^3\,\mathrm{d}x$
取 $f(z) = \frac{\mathrm{e}^{3\mathrm{i}z} - 3\mathrm{e}^{\mathrm{i}z} + 2}{z^3}$ ，由于 $\sin^3 x = \frac{3\sin x - \sin 3x}4$ ，有 $\operatorname{Im}f(x) = \frac{\sin 3x - 3\sin x}{x^3} = -4(\frac{\sin x}x)^3$
考虑 $\mathrm{I}' = \frac 12\int_{-\infty}^{+\infty}f(x)\,\mathrm{d}x$ ，则 $\mathrm{I} = -\frac 14\operatorname{Im}\mathrm{I}'$
由于 $\mathrm{e}^{3\mathrm{i}z} - 3\mathrm{e}^{\mathrm{i}z} + 2 = (1 + 3\mathrm{i}z - \frac 92z^2 + \cdots) - 3(1 + \mathrm{i}z - \frac 12z^2 + \cdots) + 2 = -3z^2 + \cdots$
所以 $z = 0$ 是分子的二级零点，即 $z = 0$ 是 $f$ 的一级极点，且上半平面无极点
则有 $\mathrm{I}' = \frac 12 \pi \mathrm{i}\sum_{\operatorname{Im}z = 0} \operatorname{Res}$
得到 $\operatorname{Res}[f,0] = -3$
因此 $\mathrm{I}' = -\frac 32\pi\mathrm{i}$ ，所以 $\mathrm{I} = -\frac 14\cdot(-\frac 32\pi) = \frac{3\pi}8$

**7.** 求下列积分：

(2) $\displaystyle\int_0^{+\infty}\frac{x}{\mathrm{e}^{\pi x}-\mathrm{e}^{-\pi x}}\,\mathrm{d}x$。

［提示：取 $f(z)=\dfrac{z}{\mathrm{e}^{\pi z}-\mathrm{e}^{-\pi z}}$，闭路 $C$ 为矩形域：$-R<\operatorname{Re}z<R,\ 0<\operatorname{Im}z<\dfrac{1}{2}$ 的边界。］
