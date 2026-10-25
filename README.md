<p align="center">
  <img src="./assets/logo.jpg" width="140" alt="zufang-guide logo" />
</p>

<h1 align="center">租房军师 · zufang-guide</h1>

<p align="center">
  把一本租房指南，拆成 18 张能直接干活的能力卡。<br/>
  An agent skill that turns a rental handbook into 18 executable playbooks.
</p>

<p align="center">
  <a href="./LICENSE"><img src="https://img.shields.io/badge/license-MIT-2ea44f" alt="license" /></a>
  <img src="https://img.shields.io/badge/cards-18-0ea5a4" alt="cards" />
  <img src="https://img.shields.io/badge/cases-12%20tested-4f46e5" alt="cases" />
  <img src="https://img.shields.io/badge/lang-中文%20%7C%20English-f97316" alt="lang" />
</p>

<p align="center">
  <a href="#中文">中文</a> · <a href="#english">English</a>
</p>

---

## 中文

事情是这样的。

前阵子帮一个朋友看租房合同，他发来一张照片，二十来条，密密麻麻。我问他，签之前看过吗。他说看了，看不懂。

这四个字我记了很久。

租房这件事，难的从来不是「你不知道该问什么」，而是「你不知道自己该问什么」。

押金为什么能扣，转租为什么无效，房东卖房你到底要不要搬，甲醛超标算不算危房，居住证要跑几趟。这些问题在网上的答案一半是过期的，一半是别的城市的。

所以我把《城市租房生存指南》那本小册子拆了，拆成 18 张能直接干活的能力卡，做成一个 Agent Skill。它不负责替你租房，它负责在你签字、付款、搬进去之前，把该问的问出来，把该引的法条引对，把该留的证据留住。

### 它能干什么

| 场景 | 它会做什么 |
|---|---|
| 「押金不退」 | 先问你金额、理由、证据、对方是谁，再给「协商 → 12315 / 住建 → 小额诉讼」的路径 |
| 「这份合同靠谱吗」 | 按八项条款逐条过，标风险等级，再查权利人、查封、抵押、居住权四项 |
| 「我这收入能租多少」 | 用「收入 − 刚性支出 − 储蓄 − 缓冲」算上限，再拿档位红线校验，给绝对上限、推荐值、差额 |
| 「年付八折靠谱吗」 | 认出租金贷，查资金监管账户，拒绝《分期服务协议》，改押一付一 |
| 「孩子要上学」 | 按「备案 → 居住登记 / 居住证 → 区教育局学位」的顺序，列材料清单，明确不保证学位 |
| 「房东擅自进门」 | 引条例第 9 条与治安管理处罚法第 47 条，给换锁、告知、报警、减租的完整动作 |

### 安装

DeepSeek Harness（DSH）用户，直接放进技能目录：

```bash
git clone https://github.com/xevil3301/zufang-guide.git ~/.agents/skills/zufang-guide
```

DSH 会在下一次对话自动发现它，不用重启。Claude Code 等读取 `SKILL.md` 的 Agent 同样可用。

### 用起来是什么感觉

它不会一上来给你一篇三千字的攻略，而是先问你四件事：

```text
你：我想用住房公积金抵扣一部分房租，怎么弄？

它：先别急着问流程，公积金租房提取是逐个城市定规矩的。
    你在哪个城市、哪个区？
    账户里大概有多少钱？给个区间就行。
    每个月缴存多少、连续缴了多久？
    本人和配偶在当地有房吗？
```

答完，它才给结论，而且结论是表格：

```text
| 账户余额 | 可提额度（需现查） | 材料 | 入口 | 频次 |
```

### 设计上的四个偏执

**一，先问诊再开方。** 缺城市、缺阶段、缺目标的时候，先问三到四个问题，每个问题都告诉你「为什么问」。首轮最多四问，问完再答。

**二，法条优先于经验。** 所有判断尽量落到条号上。民法典租赁合同章（703–734）、住房租赁条例（国令第 812 号，2025-09-15 施行）、商品房屋租赁管理办法（住建部令第 6 号），能引原文就不写「一般来说」。

**三，输出要有形状。** 押金五列，起诉四行，合同四列表。知识写成散文会被漏掉，写成表就不会，因为空格逼着你补。

**四，该现查就现查。** 三百多个城市，六套参数，每年还变。这个仓库不预置全国数据，只给「查询配方 + 官方入口 + 需现查」的标记。宁可告诉你「这条要现查」，也不给你一个看着合理的假数字。

### 能力地图

| 分组 | 能力卡 |
|---|---|
| 入口与问诊 | `triage` 场景分诊 · `intake-interview` 六槽位问诊 |
| 租前 | `budget-and-needs` 预算需求 · `affordability-model` 负担测算 · `sourcing-and-scam` 找房防骗 · `viewing-inspection` 看房体检 · `contract-review` 合同审查 |
| 租中 | `move-in-handover` 入住交接 · `community-and-maintenance` 维护沟通 · `home-safety` 居家安全 |
| 租后 | `deposit-and-move-out` 退租押金 · `sublet` 转租 · `short-stay` 短租过渡 |
| 钱与政策 | `rent-loan` 租金贷 · `public-services` 居住证学位公积金 · `city-params` 城市六参数 · `rights-and-benefits` 维权渠道 |
| 底座 | `legal-basis` 法条速查 |

每张卡都有六段：原文引用、方法论骨架、应用示例、触发场景、可执行步骤、边界。原文引用不超过 150 字，示例里凡是合成演练都会标注，不冒充真实案例。

### 测试

12 个真实场景，每个 4 条硬指标，执行 agent 与评审 agent 分开。

- 内容覆盖：**12 / 12**（每个用例都在某一轮拿到满分）
- 单轮通过：**11 / 12**（掉的那一个每次不同，重跑即满分，属于执行抖动）
- 条目通过：**47 / 48**

我没有把它写成「百分百通过」。一个会漏项的助手，比一个声称不会漏项的助手更值得信任。

### 它不做什么

买房、房贷、装修施工、代替律师出法律意见、查某城市此刻的在租房源。

### 来源与致谢

- 内容底本：《城市租房生存指南》，作者拿小多，[zufang.ababtools.com](https://zufang.ababtools.com/)
- 法条原文：民法典、住房租赁条例、商品房屋租赁管理办法、个人所得税专项附加扣除暂行办法、居住证暂行条例、治安管理处罚法、民事诉讼法、房地产经纪管理办法
- 标准：GB/T 18883-2022《室内空气质量标准》

本仓库是把一份公开指南工程化成可执行技能的尝试。原文版权归原作者，法条属公开法律文本，工程结构与提示词以 MIT 协议开放。

### License

[MIT](./LICENSE)

---

## English

Here is the thing.

A friend once sent me a photo of his rental contract, twenty-something clauses, dense as a wall. I asked if he had read it before signing. He said yes, but he did not understand it.

That answer stuck with me.

The hard part of renting is never that you do not know what to ask. It is that you do not know what you should be asking.

So I took a Chinese rental handbook and distilled it into 18 executable capability cards, packaged as an agent skill. It will not rent an apartment for you. It asks the questions you would forget, cites the statutes you would misquote, and makes you keep the evidence you will need later.

### What it covers

| Situation | What it does |
|---|---|
| Deposit withheld | Asks amount, reason, evidence, counterparty, then maps negotiation → 12315 / housing authority → small-claims court |
| Contract review | Checks eight clause groups, rates risk, then verifies owner, seizure, mortgage, and residence rights |
| Affordability | Computes a cap from income − fixed costs − savings − buffer, then cross-checks against a tier ceiling |
| Annual prepay | Detects rent loans, checks escrow accounts, refuses installment agreements, defaults to monthly payment |
| School enrollment | Orders the workflow: lease filing → residence permit → district school application, with a material checklist |
| Landlord entry | Cites the Housing Rental Regulation art. 9 and the Public Security Administration Punishments Law art. 47 |

### Install

```bash
git clone https://github.com/xevil3301/zufang-guide.git ~/.agents/skills/zufang-guide
```

For DeepSeek Harness the skill is discovered on the next turn, no restart needed. Any agent that reads `SKILL.md` can use it.

### Four design rules

1. **Interview before answering.** Missing city, stage, or goal? Ask three to four questions first, each with a reason.
2. **Statutes over folklore.** Civil Code arts. 703–734, the Housing Rental Regulation (State Council Order No. 812, effective 2025-09-15), and the Commercial Housing Lease Measures.
3. **Answers need a shape.** A five-column deposit table, a four-line litigation block, a four-column contract review. Tables force completeness.
4. **Query, do not invent.** Six parameters vary by city and change yearly. The repo ships a query recipe and official entry points, never a fabricated number.

### Testing

12 scenarios, 4 binary criteria each, executor and judge separated.

- Content coverage: **12 / 12**
- Single-run pass: **11 / 12** (the failing case rotates and passes on rerun, an execution jitter)
- Criteria: **47 / 48**

### Out of scope

Buying property, mortgages, renovation work, formal legal opinions, live listing data.

### Attribution

Source handbook: *城市租房生存指南* by 拿小多, [zufang.ababtools.com](https://zufang.ababtools.com/). Statutes are public legal texts. Engineering structure and prompts are released under MIT.

---

<p align="center"><sub>Built with the cangjie-skill distillation pipeline · 18 cards · 12 tested scenarios</sub></p>
