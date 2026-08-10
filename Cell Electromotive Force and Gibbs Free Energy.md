---
tags:
  - 电化学
  - 专题笔记
  - 吉布斯自由能
  - 电池电动势
  - 热力学自发性
---

# 电池电动势与吉布斯自由能

## 1. 自发性必须针对完整反应判断

一个半反应只描述一个电极上的电子转移：

$$
\mathrm{Ox}+ne^-\rightleftharpoons\mathrm{Red}
$$

但电子不能凭空产生或消失。持续的电化学过程必须同时包含：

- 氧化半反应：产生电子；
- 还原半反应：消耗电子。

因此不能孤立地说“某个还原半反应自发或不自发”，必须说明它与哪个氧化半反应配对，并判断完整电池反应。

---

## 2. 标准电池电动势

所有电极电位统一按还原方向查表：

$$
\boxed{
E^\circ_{\mathrm{cell}}
=E^\circ_{\mathrm{cathode,red}}
-E^\circ_{\mathrm{anode,red}}
}
$$

即使阳极实际发生氧化，代入的仍是该电对的**标准还原电位**。

> **注意：** 不要重复变号
> 如果已经使用“阴极还原电位减阳极还原电位”，就不要先把阳极数据改成氧化电位再相减，否则会重复变号。

---

## 3. 电动势与标准吉布斯自由能

完整电池反应满足：

$$
\boxed{
\Delta G^\circ=-nFE^\circ_{\mathrm{cell}}
}
$$

其中：

- $n$：配平后的完整反应转移电子数；
- $F=96485\ \mathrm{C\,mol^{-1}}$：法拉第常数。

判断关系：

$$
E^\circ_{\mathrm{cell}}>0
\Longleftrightarrow
\Delta G^\circ<0
$$

标准条件下，所写方向热力学自发。

$$
E^\circ_{\mathrm{cell}}<0
\Longleftrightarrow
\Delta G^\circ>0
$$

所写方向不自发，反方向自发。

$$
E^\circ_{\mathrm{cell}}=0
\Longleftrightarrow
\Delta G^\circ=0
$$

完整反应处于标准条件下的平衡。

> **要点：** SHE 的零点不是自由能为零
> 人为规定的是 $E^\circ_{\mathrm{SHE}}=0\ \mathrm{V}$。吉布斯自由能变化必须针对完整反应定义，不能把“SHE 电势为零”说成“SHE 的吉布斯自由能为零”。

---

## 4. 非标准条件下的完整关系

化学热力学给出：

$$
\Delta G=\Delta G^\circ+RT\ln Q
$$

能斯特方程：

$$
E_{\mathrm{cell}}
=E^\circ_{\mathrm{cell}}
-\frac{RT}{nF}\ln Q
$$

两边乘以 $-nF$：

$$
-nFE_{\mathrm{cell}}
=-nFE^\circ_{\mathrm{cell}}+RT\ln Q
$$

利用：

$$
\Delta G^\circ=-nFE^\circ_{\mathrm{cell}}
$$

得到：

$$
\boxed{
\Delta G=-nFE_{\mathrm{cell}}
}
$$

所以实际条件下应使用实际电池电动势判断方向，而不是机械地只看标准电势表。

> **注意：** 这里不是带负载时的端电压
> 式中的 $E_{\mathrm{cell}}$ 指当前温度和活度条件下的可逆平衡电动势。电池输出电流时的端电压还包含欧姆压降和极化损失，不能直接代入此式代表完整反应的 $\Delta G$。

---

## 5. Zn–SHE：两个方向的比较

标准还原电位：

$$
E^\circ_{\mathrm{Zn^{2+}/Zn}}=-0.763\ \mathrm{V}
$$

$$
E^\circ_{\mathrm{H^+/H_2}}=0\ \mathrm{V}
$$

### 假设 Zn²⁺ 还原、H₂ 氧化

完整反应：

$$
\mathrm{Zn^{2+}+H_2\rightarrow Zn+2H^+}
$$

$$
E^\circ_{\mathrm{cell}}
=-0.763-0
=-0.763\ \mathrm{V}
$$

$$
\begin{aligned}
\Delta G^\circ
&=-2F(-0.763)\\
&\approx+147\ \mathrm{kJ\,mol^{-1}}
\end{aligned}
$$

所以标准条件下该方向不自发。

准确说法是：

> 标准条件下，$\mathrm{H_2}$ 不能自发地把 $\mathrm{Zn^{2+}}$ 还原为 Zn。

不能笼统说“$\mathrm{Zn^{2+}}$ 的还原不自发”，因为换用更强的还原剂时，完整反应可能自发。

### 反方向：Zn 氧化、H⁺ 还原

$$
\mathrm{Zn+2H^+\rightarrow Zn^{2+}+H_2}
$$

$$
E^\circ_{\mathrm{cell}}
=0-(-0.763)
=+0.763\ \mathrm{V}
$$

$$
\Delta G^\circ
\approx-147\ \mathrm{kJ\,mol^{-1}}
$$

所以该方向在标准条件下热力学自发。

---

## 6. Fe³⁺/Fe²⁺–SHE 案例

先确认电对：

$$
\boxed{
\mathrm{Fe^{3+}+e^-\rightarrow Fe^{2+}}
\qquad
E^\circ=+0.77\ \mathrm{V}
}
$$

它不是 $\mathrm{Fe^{3+}/Fe}$ 电对。由于两种形态都是离子，需要 Pt 提供惰性导电界面：

$$
\mathrm{Pt\;\vert\;Fe^{3+},Fe^{2+}}
$$

与 SHE 配对时，Fe³⁺/Fe²⁺ 的还原电位更高：

- 阴极：$\mathrm{Fe^{3+}}$ 还原；
- 阳极：$\mathrm{H_2}$ 氧化。

配平后的完整反应：

$$
\mathrm{H_2+2Fe^{3+}\rightarrow2H^++2Fe^{2+}}
$$

$$
E^\circ_{\mathrm{cell}}=0.77-0=+0.77\ \mathrm{V}
$$

$$
\Delta G^\circ
=-2F(0.77)
\approx-149\ \mathrm{kJ\,mol^{-1}}
$$

因此 Fe³⁺ 在标准条件下具有氧化 H₂ 的热力学能力。

反方向的 $E^\circ_{\mathrm{cell}}=-0.77\ \mathrm{V}$，标准条件下不自发。

---

## 7. 热力学自发不等于动力学快速

即使：

$$
\Delta G^\circ<0
$$

实际反应仍可能很慢。速度还取决于：

- 电极材料和催化活性；
- 交换电流密度和电荷转移动力学；
- 活化过电位；
- 传质；
- 电极表面污染或钝化；
- 温度和有效面积。

例如 H₂ 氧化通常需要合适的催化表面；仅把 H₂ 通入 Fe³⁺ 溶液，若没有适当界面，反应可能很慢。

> **速记：** 最短记忆
> **$E$ 和 $\Delta G$ 判断方向；动力学与传质决定速度。**

---

## 8. 判断自发性的固定流程

1. 两个半反应统一写成还原方向；
2. 查清电对和标准还原电位；
3. 高还原电位作阴极，低还原电位作阳极；
4. 把阳极反应反向并配平电子；
5. 写出完整反应；
6. 计算 $E^\circ_{\mathrm{cell}}=E^\circ_\mathrm{cathode}-E^\circ_\mathrm{anode}$；
7. 用 $\Delta G^\circ=-nFE^\circ_{\mathrm{cell}}$ 判断标准自发性；
8. 非标准条件使用能斯特方程；
9. 最后单独评价动力学和实验可观察性。

## 相关笔记

- [标准电极电位、SHE与Zn-SHE电池](./标准电极电位、SHE与Zn-SHE电池.md)
- [能斯特方程与符号判断](./能斯特方程与符号判断.md)
- [极化、过电位与传质限制](./极化、过电位与传质限制.md)
- [核心公式速查](../03_复习资料/核心公式速查.md)
- [易错点汇总](../03_复习资料/易错点汇总.md)

