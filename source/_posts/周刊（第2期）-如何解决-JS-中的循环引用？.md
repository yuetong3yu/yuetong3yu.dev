---
title: 周刊（第2期）- 如何解决 JS 中的循环引用？
date: 2022-02-23 15:01:49
tags: Weekly
---

## 如何解决 JS 中的循环引用？

写了一个例子来解释循环引用：https://codesandbox.io/s/circular-dep-kviv39

看到，在最外面拿到的 a 是 `1undefined23`。

显而易见，对于 _文件 B_ 来说，引入的 a 就是一个 undefined。

**而其实正是因为 A 依赖了 B，所以导致找到 B 文件的时候，A 还没有初始化导出，因此它就是一个 undefined。**

这就是在我们代码中隐藏的循环引用的 BUG，恰恰这种 BUG 又无法被编辑器所提示出来，因此会导致运行时出错。

### 解决方案

不错的库 [Madge](https://github.com/pahen/madge) 可以检测出项目中的循环依赖，可以作为 devDependencies 来做代码提交前的检测。

![](https://tva1.sinaimg.cn/large/e6c9d24ely1gznl9s9k4yj210w06mmxn.jpg)

---

## Cool Knowledge

### `<sup>` 标签

<sup></sup> 标签用作标记文字的上标(superscript)。 （https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sup）

例如来标记平方米（m2）：`<span>m<sup>2</sup><span>`。

### Online PDF Editor

A online PDF editing platform. Good at operating, and its FREE(_important_)!

https://www.pdfzorro.com/

### How to choose last element of specific className?

```css
[class~='specific-class']:last-of-type {
  background: red;
}
```

### What is left/right-leaning?

这个要根据政治体系而言，「左」意味着贴近当前所处的社会体系，「右」意味着与当前所处的社会体系相悖。 举个例子来说：对于我国来说，“改革开发”就是一次「右倾」的尝试。因为在出现“中国特色社会主义”以前，我国人民的共识是共产主义，是国家对经济进行直接的管理和调节。那么“改革开发”这种带有浓重的市场经济/资本主义的举动，相对于当时的社会制度就是相悖的，因此称为「右」。 而另一个例子来说，“文化大革命”就是一次“极左”的运动，它使用的极端的社会活动方式来倾向共产主义。 对于西方国家而言，资本注意是它们的社会制度。所以它们的「左」，就是意味着“自由”、“经济”等西方色彩的概念。它们的「右」，就是“平等“、”共产“等社会主义的概念。

### 在墙内是否要去体制内？

看到一片不错的体制内外的对比文章，很中肯：https://mp.weixin.qq.com/s/i_ertYy-R9s6mvf2m3J6rA

---

## Investment Knowledge

### 如何使用恐贪指数和风险溢价指数来指导我们的操作？

![](https://tva1.sinaimg.cn/large/e6c9d24ely1gznlxauhkej20qc0jvdgb.jpg)

![](https://tva1.sinaimg.cn/large/e6c9d24ely1gznlxpow6cj20u019sq6z.jpg)

![](https://tva1.sinaimg.cn/large/e6c9d24ely1gznlxve91bj20u019sq78.jpg)

---

## Investment

### Operations

- 2022.2.8
  - 医药加仓 2000

### Ciscumstance

- 新能源汽车，工信瑞银 C：仓位：7.5%，收益：-2.27%；

- 中证 500，天弘中证 C；仓位：14%；收益：-7.8%；

- 沪深 300，西部利得 C：仓位：12%；收益：-8.5%；

- 医药 创新药，工银瑞信 C：仓位：64%；收益：-15.6%；
