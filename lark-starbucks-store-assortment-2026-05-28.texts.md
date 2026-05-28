# 01 适配分算法 — texts

> Edit text below. After save, run:
>   python3 assets/apply-texts.py <deck.html> <texts.md>
>
> Rules:
>   • Edit ONLY this file. Visual tweaks → overrides.css.
>     Layout / structure / new slides → re-ask Claude.
>   • Use `\n` to insert a line break (renders as <br>).
>   • Do NOT rename the slide-NN.field ids — they pair with HTML.

## slide-01 (content-2col) — 01 适配分算法
title: 给每个「门店-商品-时段」算一个适配分
tag: ALGORITHM · 决策函数
formula: 适配分 = <span class="accent">真实需求</span> * 毛利\n+ 连带销售收益\n- 损耗风险 - 缺货损失\n- 操作与约束成本
term-01: 把「卖得出去且利润高」的商品推上去
term-02: 把「卖不掉会报损、制作复杂、占空间」的商品压下来
term-03: 输出每店、每 SKU、每时段的建议备货量
input-tag: INPUT · 五类信号
input-01.title: 门店场景
input-01.body: 办公楼、社区、商场、交通枢纽，以及工作日与周末差异
input-02.title: 商品属性
input-02.body: 毛利、保质期、制作复杂度、替代关系与组合购买
input-03.title: 时段需求
input-03.body: 早餐、午间、下午茶、晚间外带，不按全天平均配货
input-04.title: 环境约束
input-04.body: 天气、节假日、配送频次、冷藏与陈列容量
decision.title: 核心修正
decision.body: 库存不准时，销量不是需求。模型要把早售罄、断货、替代购买还原成真实需求。

## slide-02 (process) — 02 三阶段落地
title: 三阶段落地路径：预测、协同、复制
step-01.num: 01
step-01.title: 基础需求预测
step-01.body: 建立每店每 SKU 每时段预测，修正缺货与库存不准，让系统看到被压制的真实需求。
step-02.num: 02
step-02.title: 店长人机协同
step-02.body: 总部下发建议备货量，店长可确认、上调或下调，并记录本地事件与调整原因。
step-03.num: 03
step-03.title: 总部反馈复制
step-03.body: 总部识别有效调整，给门店打场景标签，把策略复制到相似门店并持续回流训练。

## slide-03 (iframe-embed) — 03 系统原型 Demo
title: 系统原型 Demo：门店备货闭环工作台
