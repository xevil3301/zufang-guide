<p align="center">
  <img src="./assets/logo.jpg" width="140" alt="zufang-guide logo" />
</p>

<h1 align="center">租房军师 · zufang-guide</h1>

<p align="center">
  租房前帮你问对问题，出事时告诉你找谁。<br/>
  Ask the right questions before you sign, and know who to call when things go wrong.
</p>

<p align="center">
  <a href="./LICENSE"><img src="https://img.shields.io/badge/license-MIT-2ea44f" alt="license" /></a>
  <img src="https://img.shields.io/badge/cards-18-0ea5a4" alt="cards" />
  <img src="https://img.shields.io/badge/lang-中文%20%7C%20English-f97316" alt="lang" />
</p>

<p align="center"><a href="#中文">中文</a> · <a href="#english">English</a></p>

---

## 中文

租房这件事，普通人最容易吃两种亏。

一种是不知道该问什么。合同摆在面前，二十多条，看是看了，看不懂，签完才发现押金条款写着「卫生不达标扣全款」。

另一种是出了事不知道找谁。房东不退押金，你打 110 不对，打 12345 又说不清，最后拖到没脾气，钱就算了。

这个技能就干两件事，**先帮你想起来该问什么，再告诉你该找谁**。

### 它能帮你解决的几件事

| 你遇到的麻烦 | 它会怎么帮你 |
|---|---|
| 押金被扣，房东不给理由 | 问清金额、理由、证据，区分「正常损耗」和「人为损坏」，再给协商、投诉、起诉三条路 |
| 合同看不懂，怕签错 | 按租金、押金、租期、违约、维修等八块逐条看，标出哪条要改、怎么改 |
| 不知道房租多少算贵 | 用你的收入、固定开销、想存的钱算出上限，告诉你这个价对你合不合理 |
| 中介推年付打折、分期付 | 认出租金贷，告诉你哪些钱不能付、已经签了怎么办 |
| 居住证、孩子上学、公积金 | 按「备案 → 居住登记 → 学位/公积金」的顺序，列清楚要带什么材料 |
| 房东擅自进门、换锁 | 告诉你这违不违法、能不能换锁、报警怎么说、能不能减租 |

### 安装

DeepSeek Harness 读取 `~/.agents/skills` 目录，把这个仓库克隆进去就行，不用重启。

**Windows PowerShell**

```powershell
git clone https://github.com/xevil3301/zufang-guide.git "$HOME\.agents\skills\zufang-guide"
```

**macOS / Linux**

```bash
git clone https://github.com/xevil3301/zufang-guide.git ~/.agents/skills/zufang-guide
```

装好后直接问它问题就行，比如「房东不退押金怎么办」「这份合同帮我看看」。其他能读 `SKILL.md` 的 Agent 也能用。

### 它不会一上来就给你一篇长文

它会先问你几个问题，比如城市、押金多少、合同和转账还在不在、对方是房东还是二房东。问完才给结论，因为少一个信息，答案就可能反。

### 它不做什么

买房、房贷、装修施工、代替律师出法律意见、查某个城市此刻的在租房源。

### 来源

内容底本：《城市租房生存指南》，作者拿小多，[zufang.ababtools.com](https://zufang.ababtools.com/)。法条引自民法典、住房租赁条例、商品房屋租赁管理办法等公开文本。工程结构以 MIT 协议开放。

---

## English

Renting has two classic traps.

You do not know what to ask, so you sign a lease you cannot read and find out later that the deposit clause says the landlord keeps everything if the cleaning is not up to standard.

Or something goes wrong and you do not know who to call. The landlord keeps your deposit, and you bounce between hotlines until you give up.

This skill does two things. **It reminds you what to ask, and it tells you who to call.**

### What it handles

| Problem | What it does |
|---|---|
| Deposit withheld | Separates normal wear from damage, then maps negotiation, complaint, and small-claims court |
| Lease you cannot read | Reviews eight clause groups and marks what to change |
| Is this rent too high | Computes your affordable cap from income, fixed costs, and savings goals |
| Annual prepay and installment plans | Detects rent loans and tells you what not to pay |
| Residence permit, school, housing fund | Orders the paperwork and lists the documents |
| Landlord entering without notice | Explains your options, from changing the lock to calling the police |

### Install

DeepSeek Harness discovers skills in `~/.agents/skills`.

**Windows PowerShell**

```powershell
git clone https://github.com/xevil3301/zufang-guide.git "$HOME\.agents\skills\zufang-guide"
```

**macOS / Linux**

```bash
git clone https://github.com/xevil3301/zufang-guide.git ~/.agents/skills/zufang-guide
```

Then just ask. Any agent that reads `SKILL.md` can use it too.

### It asks before it answers

City, deposit amount, evidence, and who the other side is. Without those, the answer can point the wrong way.

### Out of scope

Buying property, mortgages, renovation, formal legal opinions, and live listing data.

### Attribution

Source handbook: *城市租房生存指南* by 拿小多, [zufang.ababtools.com](https://zufang.ababtools.com/). Statutes are public legal texts. Engineering structure released under MIT.

---

<p align="center"><sub>18 capability cards · bilingual · MIT</sub></p>
