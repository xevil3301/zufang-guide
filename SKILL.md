---
name: zufang-guide
description: |
  用户要租房、找房、看房、签合同、入住、退租、转租、押金纠纷、租房维权、租房补贴或公积金提取时使用；
  也用于「房租占收入多少合适」「怎么防二房东/黑中介」「退租押金被扣怎么办」这类具体问题。
  English triggers: renting an apartment in China, lease review, rental deposit dispute, sublet, landlord refusing refund, rental subsidy.
  信息不全时先问诊：缺城市/区、缺阶段（签没签、付没付）或缺目标（省钱/维权/办事）时，先用 3–5 个问题补齐六槽位，再回答；不得用通用结论代替问诊。
  不适用于：买房/房贷、装修施工与设计、代替律师出具法律意见、查询某城市实时房源与价格（需现查）。
metadata:
  cangjie.generated-by: cangjie-tools v2.5.0
  cangjie.variant: single
  cangjie.bundle-id: bundle.zufang-guide
  cangjie.capability-count: 18
  cangjie.entrypoint-count: 1
---
# 《城市租房生存指南》 — 全书能力入口

## 触发与不触发

**适用**：与本书能力域相关的咨询与任务（见下方路由表的意图列）。
**不适用**：
- 买房、房贷、房产投资与落户政策。
- 装修施工图、材料采购与施工队管理。
- 代替律师出具法律意见、代理诉讼或出具鉴定结论。
- 查询某一城市此刻的实时房源、租金行情与在租列表（本技能只给方法与口径，实时数据需现查）。

## 核心原则（常驻速览，概览类问题读到这里即可回答）

1. 先算可支配余额再算房：用「收入 − 刚性支出 − 储蓄 − 缓冲」算出租金上限，比例红线只是上限，不是目标；低收入区间（月入 3–5k）超过 30% 即判定不合理。
2. 先验真假再谈价：官方备案平台优先，看房前不交任何费用，核对房产证与身份证，警惕二房东与黑中介。
3. 一切承诺写进合同：租金、押金、租期、维修、违约、隐性费用白纸黑字，口头承诺不算数。
4. 全程留痕：看房、交接、缴费、沟通都拍照或留下文字记录，退租和维权才有据可依。
5. 出问题按顺序升级：协商 → 社区调解 → 12315/房管/住建 → 12348 法律援助 → 法院诉讼。
6. 安全与合法性优先：不签租售一体、不租违建隔断群租、不碰未经房东同意的非法转租。
7. 以法条为准：押金扣减、转租、维修、备案、非居住空间出租，以《民法典》租赁合同章与《住房租赁条例》（2025-09-15 施行）为底线，经验说法与地方政策不得对抗法条。
8. 先查册再签约，未命中走分诊：不动产登记（权利人/查封/抵押/居住权）四项核完再付钱；超出覆盖的场景先查法条，再走 12348/12345/110，不硬套。

## 能力路由（先读本表，按意图加载 1 张能力卡）

| 用户意图 | 先读 | 补读/备注 |
|---|---|---|
| 押金不退怎么办；合同靠谱吗；我想租房但预算不多；帮我看看这个；我们这边房租太贵 | references/capabilities/intake-interview.md | references/capabilities/triage.md、references/capabilities/city-params.md、references/capabilities/affordability-model.md |
| 我该租多少钱的房子；合租还是整租；租房预算怎么定；选房要考虑哪些因素 | references/capabilities/budget-and-needs.md | references/capabilities/affordability-model.md、references/capabilities/sourcing-and-scam.md、references/capabilities/viewing-inspection.md |
| 这个房租合不合理；我这收入能租多少钱；月入四千五能租一千五吗；房租占收入多少算高；还要存钱怎么定房租 | references/capabilities/affordability-model.md | references/capabilities/budget-and-needs.md、references/capabilities/contract-review.md |
| 去哪里找房源；怎么判断真假房源；怎么识别二房东和黑中介；中介费怎么谈 | references/capabilities/sourcing-and-scam.md | references/capabilities/viewing-inspection.md、references/capabilities/contract-review.md |
| 看房要看什么；看房清单；怎么判断房子有没有问题；看房要问房东什么 | references/capabilities/viewing-inspection.md | references/capabilities/sourcing-and-scam.md、references/capabilities/contract-review.md |
| 帮我看看这份租房合同；租房合同要注意什么；押金条款怎么写；房东要卖房让我搬走怎么办；怎么和房东谈条款 | references/capabilities/contract-review.md | references/capabilities/sourcing-and-scam.md、references/capabilities/deposit-and-move-out.md |
| 刚拿到钥匙要做什么；入住要拍哪些照片；宽带和水电燃气怎么开通；租房要办居住登记吗 | references/capabilities/move-in-handover.md | references/capabilities/deposit-and-move-out.md、references/capabilities/community-and-maintenance.md |
| 东西坏了怎么报修；房东不修怎么办；合租室友矛盾怎么处理；和房东怎么沟通 | references/capabilities/community-and-maintenance.md | references/capabilities/move-in-handover.md、references/capabilities/rights-and-benefits.md |
| 退租流程；押金不退怎么办；房东乱扣押金；退租要注意什么 | references/capabilities/deposit-and-move-out.md | references/capabilities/move-in-handover.md、references/capabilities/rights-and-benefits.md |
| 我想转租；转租要房东同意吗；转租协议怎么写；房东不同意转租怎么办 | references/capabilities/sublet.md | references/capabilities/contract-review.md、references/capabilities/deposit-and-move-out.md |
| 租房纠纷怎么维权；房东不退押金找谁；黑中介怎么投诉；应届生租房补贴怎么申请；租房公积金怎么提取 | references/capabilities/rights-and-benefits.md | references/capabilities/deposit-and-move-out.md、references/capabilities/contract-review.md |
| 独居怎么保证安全；租房要买什么安防设备；门锁不放心怎么办 | references/capabilities/home-safety.md | references/capabilities/move-in-handover.md |
| 押金扣减合法吗；转租需要房东同意吗；房东不修怎么办；房东卖房我还能住吗；隔断房违法吗 | references/capabilities/legal-basis.md | references/capabilities/contract-review.md、references/capabilities/deposit-and-move-out.md、references/capabilities/sublet.md、references/capabilities/rights-and-benefits.md |
| 只租一两个月；短租不用签合同吧；过渡住哪里；月租公寓怎么选 | references/capabilities/short-stay.md | references/capabilities/contract-review.md、references/capabilities/move-in-handover.md、references/capabilities/rent-loan.md |
| 年付打折靠谱吗；分期付房租；租金贷是什么；长租公寓跑路怎么办 | references/capabilities/rent-loan.md | references/capabilities/sourcing-and-scam.md、references/capabilities/contract-review.md、references/capabilities/legal-basis.md |
| 租房能办居住证吗；孩子能上学吗；房租抵个税怎么填；公积金怎么提取 | references/capabilities/public-services.md | references/capabilities/move-in-handover.md、references/capabilities/rights-and-benefits.md、references/capabilities/legal-basis.md |
| 我这种情况该看什么；这算谁的；该找谁；超出范围怎么办 | references/capabilities/triage.md | references/capabilities/legal-basis.md、references/capabilities/rights-and-benefits.md |
| 我们这城市居住证要什么材料；孩子能上哪所学校；公积金能提多少；这个城市短租合法吗；当地押金受监管吗 | references/capabilities/city-params.md | references/capabilities/public-services.md、references/capabilities/rights-and-benefits.md、references/capabilities/short-stay.md、references/capabilities/rent-loan.md |

**非能力类查询**：
- 书名/作者/章节/整书概览 → references/overview.md
- 术语解释 → references/glossary.md
- 决策规则速查（不需要原文依据时） → references/cheatsheet.md
- 完整意图与关键词索引（本表未覆盖的意图先查这里） → references/capability-index.md

## 加载规则

- 每次任务先读本文件，再按路由表加载 **1** 张能力卡；任务明确跨域时最多加载 2 张。
- 概览/书名类问题不加载能力卡，用「核心原则」与 overview.md 回答。
- 路由表与 capability-index.md 都无法命中的意图，明确告知超出本书范围，不要硬套。

## 边界与判停

- 出现人身安全威胁（家暴、跟踪、入室、威胁恐吓）时，先保证安全并报警 110，再处理租约问题。
- 对方要求「先交定金/押金才能看房」或拒绝出示房产证与身份证时，停止交易。
- 发现违建、隔断房、群租或消防通道堵塞时，不签约，向 12345 / 96119 举报。
- 用户只给一句话、缺城市/区、缺阶段或缺目标时，先按 intake-interview 问 3–5 个问题；信息不足不得直接给具体金额或结论。

## 高频必答清单（入口常驻，任何情况下都要覆盖）

1. 短租：707 六个月以上应书面；不写期限=不定期、可随时解除（730）；押金收据+交接单；月租公寓/服务式/转租三选；少于 7 天改酒店。
2. 二房东：716 转租需同意；718 知道转租六个月未异议视为同意；719 次承租人可代付；717 不得超剩余租期；报警/诉讼/12345；条例 19/20 资金监管。
3. 甲醛：GB/T 18883-2022 密闭 12 小时、0.08 mg/m³；CMA 检测；731 可随时解除；合同写空气质量；通风有效，绿植/活性炭/柚子皮无效。
4. 租金贷：租金贷占租金收入不超 30%；单次收租>3 个月或押金>1 个月超额监管；见《分期服务协议》即拒签并改押一付一；已签保留合同投诉 12315/住建。
5. 个税：住房租金 1500/1100/800 元每月；与房贷利息不兼得；合同信息留存 5 年；按实际租期申报。
6. 居住证/学位：居住半年 + 合法稳定就业/住所/连续就读之一；备案免费、房东不办承租人可自办；学位按区政策与积分、不保证；材料含户口簿、出生证、接种证。
7. 擅自进入：条例 9 不得擅自进入；可自费换锁芯并书面告知；报警可引治安管理处罚法 47 条第 3 项；可主张减租或解除。
8. 查封：724 可解除并返还租金押金；签约前查册四项（权利人/查封/抵押/居住权）；查封不当然无效，房东隐瞒可依 148 撤销。
9. 改造/养宠：715 经书面同意可改善；710 正常损耗不赔；违约可能恢复原状或赔偿；可用可移除装置替代。
10. 跳单/中介费：965 跳单可能违约；条例 26、经纪办法 18 明码标价、不得加价；保留带看确认书；12315/住建投诉。
11. 违约金：585 过分高于损失可调减（超损失 30% 一般认定过高）；押金与违约金不重复；房东举证实际损失；协商/调解/诉讼。
12. 起诉：管辖（房屋所在地/被告住所地）；188 三年时效；165 小额诉讼 50% 线以下一审终审；证据清单（合同/转账/聊天/照片/备案）。

> 回答末尾逐条对照本清单，缺项补上；无法判断的写「需现查」。
