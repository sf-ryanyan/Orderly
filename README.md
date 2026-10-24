<div align="center">

# Orderly

**Multi-Store Requisition & Central Fulfillment**

*Stores order by usage · The central kitchen aggregates and plans · HQ reconciles at month end*

[![Live Demo](https://img.shields.io/badge/Live_Demo-Open-D9C08E?style=for-the-badge)](https://sf-ryanyan.github.io/Orderly/)
[![Single File](https://img.shields.io/badge/Single_File-HTML-2A3566?style=for-the-badge)](#technical-notes)
[![No Build](https://img.shields.io/badge/No_Build-No_Backend-2A3566?style=for-the-badge)](#technical-notes)

### ▶ **[Open the live demo](https://sf-ryanyan.github.io/Orderly/)**

**English** · [中文](#中文)

</div>

---

## What this is

Most food businesses hit the same wall at the third location: **stores order over WeChat, the central kitchen guesses, and month end turns into an argument.**

Orderly is a working demo that walks the whole chain end to end — what the stores need, how much the central kitchen has to produce and purchase, how it gets delivered, whether it actually arrived, and whose cost it was.

**It is not a mockup and not a slide deck.** The order you place in the store view genuinely appears in the central kitchen's aggregated demand, and genuinely appears in HQ's reconciliation table. Three roles, one shared dataset.

---

## 🎯 The problem it solves

| What it looks like today | What it costs you |
|---|---|
| A store manager sends *"send me 5 cases of oranges tomorrow"* over WeChat | No record. Afterwards nobody can prove who asked for what |
| The central kitchen plans production by feel | Overproduce and it spoils; underproduce and stores run dry |
| No cutoff time, so people keep adding to the order | Production schedules get reworked, purchasing can't keep up |
| Ordered quantity and delivered quantity don't match | The store says it was short, the kitchen says it shipped — no evidence either way |
| Internal transfers and outside purchases sit in one pile | True store-level cost is unknowable, and so is the kitchen's output value |
| Every store orders on its own, nobody compares prices | The same item costs different amounts from different suppliers and nobody notices |

**If three of these six are true for you, this system pays for itself.**

---

## ⚙️ How it works

### Store manager — no memory, no guesswork

- **Suggested order quantity, calculated** — from *four-week average usage + safety stock − current stock*
- **Below-safety-stock items flag themselves**, so the manager doesn't have to watch for it
- **Cross-supplier price comparison** — when a cheaper supplier carries the same item, the card says so and switches in one click
- **Smart Fill** — fills the cart to the suggested quantities *and* switches to the cheaper suppliers in one action
- **Budget bar updates live**, and anything over the auto-approval limit is routed to a manager

### Central kitchen — today's production on one screen

- **Every store's demand merged automatically**; expand any line to see which store asked for what
- **In-house production** and **outside purchasing** split into separate columns with separate workflows
- **Delivery notes generated in one click**, broken down per store

### Receiving — shortages stop being a grey area

- Confirm each line as it arrives
- **Report a shortage directly** — the system raises a replenishment order and folds it into the next run
- Everything is on the record, so stores and the kitchen stop arguing about what shipped

### HQ — month end stops taking a week

- Today at a glance: stores ordered, total value, any exceptions
- **Monthly reconciliation** — internal transfers and outside purchases calculated separately, with internal share per store
- Central kitchen output value tracked on its own line

---

## 🕹 Try it in two minutes

| Step | What to do |
|---|---|
| **1** | Pick the industry closest to your business — juice, bakery, boba, Chinese restaurant or grocery — and enter as **Store Manager** |
| **2** | Hit **Smart Fill**, watch the cart and budget bar move, then read the savings summary after you submit |
| **3** | Click **"See what the central kitchen received"** — your order is now in the aggregate |
| **4** | Generate delivery notes, switch back to the store and confirm receipt — one line comes up short on purpose, watch it become a replenishment order |
| **5** | Switch to **Owner** and read today's orders and the monthly reconciliation |

Reset or change industry any time from the header. **All data is sample data.**

---

## 👥 Who it's for

| This system earns its keep when |
|---|
| **Three or more locations**, with a central kitchen, central warehouse or own production facility |
| Stores draw from **your own kitchen** *and* buy from **outside suppliers** |
| Ordering today runs on **WeChat, phone calls, paper or scattered spreadsheets** |
| You need **true per-store cost** at month end, or numbers an investor will look at |
| You're opening more locations and **worried coordination will break** |

A single location doesn't need this — what it solves is the coordination cost that arrives with the second and third store.

---

## 🔧 From demo to production

What you're looking at runs on sample stores, sample products and sample suppliers.

A real deployment is built around your business:

- Your own product list, units, suppliers and pricing
- Your own locations, permissions and approval rules
- Connected to live inventory, ordering and finance data
- Extended as needed — barcode receiving, supplier integration, cost dashboards, a mobile app

**It can start small** — in-house items only, for example — prove itself, then widen.

---

## Technical notes

- One self-contained HTML file. No install, no build step, no backend
- Five industries, three roles, twelve products per industry, 37 hand-drawn SVG icons
- Chinese and English on screen together throughout
- Works on desktop, tablet and phone
- All state lives in the browser session — refresh resets it, nothing is uploaded anywhere

---

## About

**Designed and built by Ryan Yan** · Data Analyst

Market data and systems delivery. Requirements, interface design and interaction were all done by me.

Other demos built the same way — a clickable thing first, so the client can see it before we talk about building it — include a clinic client-management console, an agent marketing-materials ordering site, and a kitchen cabinet refacing quote tool.

---

## Disclaimer

This is a **demonstration build**. Every store, product, price, supplier and order in it is fictional sample data and represents no real business. "Orderly" is a fictional brand name used for this demo. Nothing shown here is a commercial offer.

---
---

<div align="center">

# 中文

**多门店要货与中央配货系统 · 演示版**

*门店按用量下单 · 中央厨房自动汇总排产 · 月底内部成本一笔清*

### ▶ **[打开在线演示](https://sf-ryanyan.github.io/Orderly/)**

[English](#orderly) · **中文**

</div>

---

## 这是什么

很多餐饮生意做到第三家店，都卡在同一个地方：**门店要货靠微信，中央厨房靠猜，月底算账靠吵。**

Orderly 把「门店要什么 → 中央做多少、买多少 → 怎么送 → 收没收到 → 这笔算谁的」这条链，完整地走通了一遍。

**它不是截图，也不是方案书。** 你在门店视角下的那一单，会真的出现在中央厨房的汇总里，也会真的出现在总部的对账表里。三个角色，共用一份数据。

---

## 🎯 它解决的痛点

| 现实中的样子 | 代价是什么 |
|---|---|
| 店长微信发一句「明天给我来 5 箱橙子」 | 没有记录，事后谁也说不清谁要了什么 |
| 中央厨房凭感觉排产 | 做多了烂掉，做少了缺货，两头都是钱 |
| 没有截单时间，随时有人加单 | 排产反复改，采购跟不上 |
| 要了多少、送了多少对不上 | 门店说少送了，厨房说送了，谁都没证据 |
| 内部调拨和外部采购混在一笔账里 | 门店真实成本算不清，中央厨房产值也算不清 |
| 每家店各订各的，没人比价 | 同一个商品不同供应商的差价，没人管 |

**这六条里中了三条，这套系统就值得做。**

---

## ⚙️ 它怎么解决

### 门店端 —— 不靠记性，不靠拍脑袋

- **建议订量自动算** —— 依「近四周平均用量 ＋ 安全库存 − 现有库存」得出
- **低于安全库存自动标红**，不用店长自己盯
- **跨供应商比价** —— 同一商品有更便宜的供应商时直接提示，一键切换
- **一键智能补货** —— 按建议量填满购物车，并自动换到更低价的供应商
- **预算条实时变化**，超出自动审批额度的自动转经理审批

### 中央厨房端 —— 一屏看完今天要做多少

- **各店需求自动合并**，点任意一行展开看哪家店要了多少
- **自制品排产** 与 **外部采购** 分成两栏，各走各的流程
- **一键生成配送单**，按门店拆分装车清单

### 门店收货 —— 异常不再是糊涂账

- 配送到店后逐项确认
- **少送可直接报缺**，系统自动生成补单并入下一批次
- 全程留痕，门店和厨房不用再为「到底送没送」争论

### 总部端 —— 月底不用再对一个星期的账

- 今日概览：几家店下单、总额多少、有没有异常
- **月度对账表** —— 内部调拨与外部采购分开计算，附内部占比
- 中央厨房产值单独成账

---

## 🕹 两分钟体验完整流程

| 步骤 | 做什么 |
|---|---|
| **1** | 选一个最接近你生意的行业（果汁轻食 / 烘焙 / 奶茶 / 中餐馆 / 便利超市），以**门店店长**进入 |
| **2** | 点**一键智能补货**，看购物车和预算条的变化，提交后看收益小结 |
| **3** | 点**「看看中央厨房收到了什么」**，你刚才那一单已经在汇总里了 |
| **4** | 生成配送单，切回门店确认收货 —— 系统安排了一项少送，看它怎么转补单 |
| **5** | 切到**总部**，看今日订单与月度对账 |

随时可从顶部重置或更换行业。**所有数据均为示例数据。**

---

## 👥 适合什么样的生意

| 符合这些特征，这套系统的价值最大 |
|---|
| **三家店以上**，并且有中央厨房、中央仓或自有工厂 |
| 门店既从**自家中央厨房拿货**，也向**外部供应商采购** |
| 现在的要货方式是**微信、电话、纸单或各管各的表格** |
| 月底需要算清**各门店真实成本**，或需要给投资人看数据 |
| 正在扩店，**担心店一多就管不过来** |

单店暂时用不上 —— 它解决的是第二、第三家店带来的协调成本。

---

## 🔧 从演示到真系统

你现在看到的是演示版，用的是示例门店、示例商品、示例供应商。

**真正落地时会按你的生意定制：**

- 换成你自己的商品清单、单位、供应商与价格
- 换成你自己的门店、权限与审批规则
- 接上真实的库存、订单与财务数据
- 按需扩展：扫码收货、供应商直连、成本看板、手机端

**可以先从一个小范围开始** —— 比如只做自制品的要货与汇总 —— 跑通了再往外扩。

---

## 技术说明

- 单个自包含 HTML 文件，无需安装、无需构建、无需后端
- 五个行业、三个角色、每个行业 12 个商品、37 个手绘 SVG 图标
- 全站中英双语同屏
- 桌面、平板、手机均可使用
- 所有状态仅存在于当前浏览器会话，刷新即重置，不上传任何信息

---

## 关于

**设计与开发：Ryan Yan** · Data Analyst

做市场数据与系统落地。本项目的需求梳理、界面设计与交互实现全部由本人完成。

同类演示还有几套 —— 诊所客户管理中控台、经纪人物料下单系统、橱柜改造报价工具 —— 都是同一个做法：**先做一个能点的东西，让客户看懂了再谈怎么做。**

---

## 说明

本项目为**演示版本**。其中的门店、商品、价格、供应商与订单数据均为虚构示例，不代表任何真实企业。「Orderly」为本演示使用的虚构品牌名称。本页内容不构成任何商业要约。
