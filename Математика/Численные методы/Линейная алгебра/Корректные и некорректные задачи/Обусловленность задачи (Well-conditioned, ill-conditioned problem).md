Рассмотрим СЛАУ $$Ax=b$$где $A$ - квадратная матрица. Пусть правая часть получит возмещение $\Delta b$, тогда решением будет $x+\Delta x$:$$A(x+\Delta x)=b+\Delta b$$Выразим $\Delta x$:$$\begin{gather}
Ax+A\Delta x=b+\Delta b \\
A\Delta x=\Delta b \\
\Delta x=A^{-1}\Delta b
\end{gather}$$Тогда по условию [[Согласованная норма (Consistent norm)|согласованности нормы]] получим:$$\begin{gather}
\lVert\Delta x\rVert\leq\lVert A^{-1}\rVert\ \lVert\Delta b\rVert \\
\lVert b\rVert\leq\lVert A\rVert\ \lVert x\rVert
\end{gather}$$Объединим неравенства:$$\begin{gather}
\lVert b\rVert\ \lVert\Delta x\rVert\leq\lVert A^{-1}\rVert\ \lVert\Delta b\rVert\ \lVert A\rVert\ \lVert x\rVert \\
\frac{\lVert\Delta x\rVert}{\lVert x\rVert}\leq\lVert A^{-1}\rVert\ \lVert A\rVert\frac{\lVert\Delta b\rVert}{\lVert b\rVert}
\end{gather}$$Получили соотношение **относительных погрешностей** измерения $\frac{\lVert\Delta b\rVert}{\lVert b\rVert}$ и решения $\frac{\lVert\Delta x\rVert}{\lVert x\rVert}$.

Число $\text{cond} A$ называется **числом обусловленности** матрица $A$ и равно:$$\text{cond} A=\lVert A\rVert\ \lVert A^{-1}\rVert$$Чем **больше** $\text{cond} A$, тем хуже обусловлена матрица и тем **сильнее** сказываются на решении СЛАУ ошибки в исходных данных.

Удобное правило **приближённой** оценки решения СЛАУ:
Если **число обусловленности** $\text{cond} A=O(10^p)$, и исходные данные имеют **погрешность** в $l$-м знаке после запятой, то **независимо** от метода решения в результате можно гарантировать **не более** $l-p$ знаков после запятой.

Справедлива **оценка** числа обусловленности снизу:$$\text{cond} A=\lVert A\rVert\ \lVert A^{-1}\rVert\geq\lVert AA^{-1}\rVert=\lVert E\rVert=1$$В силу [[Согласованная норма (Consistent norm)|соотношения]] $\lVert A\rVert\geq\max|\lambda|$ получим другую оценку  числа обусловленности, которая не зависит от выбранной нормы:
$$\text{cond} A=\lVert A\rVert\ \lVert A^{-1}\rVert\geq\max|\lambda|\frac{1}{\min|\lambda|}$$**Вывод**: на число обусловленности оказывает значительное негативное влияние наличие очень маленьких собственных чисел (коротких собственных векторов).