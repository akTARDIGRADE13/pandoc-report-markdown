---
title: "サンプルドキュメント"
author: "GPT-4o"
date: \today
bibliography: references.bib
---

# イントロダクション

このドキュメントは、Pandocを使用してMarkdownからPDFに変換する際のスタイルを確認するための物理学に関連したサンプルです。ChatGPTに吐かせたサンプルですので、内容の正確さに関しては一切保証しません。


## 外部ファイルの挿入
外部ファイルを挿入する例を示します。

``` {.include}
chapter1.md
chapter2.md
```

## Pythonを使った数値解析の例

ニュートン法を用いて関数の根を求めるPythonコードの例を示します。

```python
import numpy as np

def f(x):
    return x**2 - 2

def df(x):
    return 2*x

def newton_method(x0, tol=1e-10, max_iter=100):
    x = x0
    for i in range(max_iter):
        x_new = x - f(x)/df(x)
        if abs(x_new - x) < tol:
            break
        x = x_new
    return x

root = newton_method(1.0)
print(f"squred 2: {root}")
```

## 力学におけるベクトル場の描画

TikZを使用して二次元のベクトル場を描画する例を示します。

```tikz
\begin{tikzpicture}
\draw[->] (-2,0) -- (2,0) node[below right] {$x$};
\draw[->] (0,-2) -- (0,2) node[above left] {$y$};
\foreach \x in {-1.5,-1,...,1.5}
    \foreach \y in {-1.5,-1,...,1.5}
        \draw[->, blue] (\x,\y) -- (\x+0.5*\x,\y+0.5*\y);
\end{tikzpicture}
```

## 量子力学におけるシュレディンガー方程式

量子力学の基本方程式であるシュレディンガー方程式を数式として表示します。

:::screen
時間依存シュレディンガー方程式は次のように表されます。

$$
i\hbar \frac{\partial \psi(x,t)}{\partial t} = \left( -\frac{\hbar^2}{2m} \nabla^2 + V(x) \right) \psi(x,t)
$$

ここで、$i$は虚数単位、$\hbar$はディラック定数、$\psi(x,t)$は波動関数、$V(x)$はポテンシャルエネルギーです。
:::

## 証明の例

数学的な証明を示します。

:::proof
ベクトルの内積は次のように定義されます。

$$
\vec{a} \cdot \vec{b} = |\vec{a}| |\vec{b}| \cos\theta
$$

ここで、$\theta$はベクトル$\vec{a}$と$\vec{b}$の間の角度です。この定義から、内積が0になる条件は$\theta = \frac{\pi}{2}$すなわち、ベクトル$\vec{a}$と$\vec{b}$が直交する場合です。
:::

## 実験データの可視化

以下に、実験データを表形式で示します。これは、ある物理実験で得られたデータです。

| 時間 (s)  | 距離 (m) |
|-----------|----------|
| 0.0       | 0.0      |
| 1.0       | 9.8      |
| 2.0       | 19.6     |
| 3.0       | 29.4     |
| 4.0       | 39.2     |

## 実験装置の構造図

以下に、実験装置の構造を図として示します。

![実験装置の構造図](./test.jpg)

## 文献引用の例

物理学の理論は多くの文献に基づいています。たとえば、次のように文献を引用できます [@sample1].

複数個の文献を引用することも可能です[@sample2] [@sample3].

## 関連リンク

さらに詳しい情報が必要な場合は、[量子力学のWikipediaページ](https://en.wikipedia.org/wiki/Quantum_mechanics)をご覧ください。


## 参考文献
