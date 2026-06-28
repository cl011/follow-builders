# AI Builders 中文日报 — 2026年6月28日

## X / Twitter

**Sam Altman** — OpenAI CEO
OpenAI 更新了 ChatGPT 中使用的 5.5 instant 模型，Altman 表示喜欢它新的"氛围感"。他提及 token 用量目前还不是"随便吃"，但团队正在努力推进。对于近日推出的 GPT-5.6，他转发了团队的发布公告，表示"团队出色完成了任务（team cooked, spicily）"。
- https://x.com/sama/status/2070612055225483692
- https://x.com/sama/status/2070614666288795703

**Dan Shipper** — Every CEO
GPT-5.6 Sol 正式发布，但根据美国政府指令，目前访问权限仅限约 20 家预批准企业，Every 并不在名单之列。Shipper 表示理解政府对 AI 安全的关切，但强调广泛的民主化访问对于美国在 AI 竞争中保持领先至关重要，并呼吁尽快向更多开发者和独立创作者开放。
- https://x.com/danshipper/status/2070554118146412979

**Aaron Levie** — Box CEO
Levie 对 GPT-5.6 印象深刻，认为它在需要大量 tool use 的知识工作者任务和长期运行的 agent 场景中表现非常强劲。他直接表示："我们现在在 AI 进展上没有遇到任何瓶颈。"
- https://x.com/levie/status/2070563281916620895

**Garry Tan** — Y Combinator 总裁 & CEO
Tan 公开批评某模型的发布方式，称"这绝对不是发布模型的正确方式，继续这样下去只会毁掉所有小型创业公司的创新土壤"。他认为这种封闭式的发布策略正在扼杀生态系统中的早期创新。
- https://x.com/garrytan/status/2070699046939820223

**Peter Yang** — AI 内容创作者
Yang 提出了一个值得思考的悖论：我们发布了 frontier model，它们被蒸馏成便宜的开源模型，美国公司转而采用这些开源模型，然后 frontier model 开始限制访问——这最终究竟会导致美国公司创新减少，还是会让开源模型更具吸引力？他还指出，资金正在从纯软件转向"服务+软件"的组合，用户要的是结果而非工具。
- https://x.com/petergyang/status/2070633838146134219
- https://x.com/petergyang/status/2070568705365577990

**Guillermo Rauch** — Vercel CEO
Rauch 强调 agent 的可观测性（observability）是构建 AI 产品的核心挑战。Agent 不仅因为 AI 模型的非确定性难以调试，还因为它们是涉及多步骤计算、多个 API 服务的复杂分布式系统。Vercel 团队为此专门优化了开箱即用的 observability 体验，目前反馈火爆。
- https://x.com/rauchg/status/2070676383135834334

**Swyx** — AI 开发者/内容创作者
Swyx 宣布接管旧金山的一个新媒体实验室，将打造面向"工程师创作者"的第三空间，意外发现实验室内附带了一个完整配线的数据中心机架，正在征询关于这个机架该如何使用的建议。他还与 Basil 合作，正在筹备首届 AI FDE（Field Deployment Engineering）小型会议。
- https://x.com/swyx/status/2070748857441362056
- https://x.com/swyx/status/2070606851377672675

**Cat Wu** — Anthropic Claude Code & Cowork 产品团队
Wu 分享了她最喜欢的 Claude Code 桌面功能之一：分屏模式（split screen），让同时处理多个任务变得更加高效自然。
- https://x.com/_catwu/status/2070613405237432766

**Thibault Sottiaux** — OpenAI Codex & ChatGPT 产品团队
OpenAI 为所有 Codex 用户提供了免费的用量重置，并表示已采取部分缓解措施；目前调查未发现大规模用户受影响的情况，团队仍在持续监测。
- https://x.com/thsottiaux/status/2070653282440405046

**Nikunj Kothari** — FPV Ventures 合伙人
Kothari 回应了外界对 AI 缺乏"taste"（品位）的批评——他指出，这些批评者大多自己从未真正构建过任何东西。真正的品位只能通过在竞技场上不断迭代来磨练，就像厨师做菜经过上百次尝试才能做出出色作品；他相信 AI 也有机会通过足够多的迭代真正发展出属于自己的 taste。
- https://x.com/nikunj/status/2070649602953576825

**Peter Steinberger** — OpenClaw & OpenAI
Steinberger 吐槽 Apple 的 notarization 流程每年多次失效，每次都需要开发者手动登录并接受新的法律协议，严重影响开发体验。
- https://x.com/steipete/status/2070626638887555227

---

## Podcasts

**No Priors**
《为什么传统 benchmark 无法评估现代 AI 模型》— 嘉宾：OpenAI 研究科学家 Noam Brown

Noam Brown 是 AI 推理领域（inference-time scaling）的先驱，他在节目中指出当前 AI 评估体系存在根本性缺陷：现有的 benchmark 没有控制 test-time compute 的用量。在 GPT-3 时代，给模型更多计算预算几乎无济于事；但现在，模型的能力已经是投入计算量的函数——给它 $10,000 的预算，它能做的事情远超 $10 时的水平。在不控制 token 用量或成本的情况下对比不同模型，结果本质上是没有意义的。

他以 GPT-5.5 为例说明：benchmark 上的提升看似有限，但控制 thinking 时间后，5.5 的效率提升极为显著。更令人担忧的是，当前各大 AI 实验室的安全评估框架（responsible scaling policies）同样没有考虑 test-time compute 因素，可能严重低估了前沿模型在高计算预算下的真实能力和潜在风险。

Brown 建议未来 benchmark 应以 token 数量或计算成本为 x 轴呈现性能曲线，而非简单的单一分数。他个人喜欢用"给 AI 编写扑克 bot"来评估模型进步：GPT-5.5 已经能在少量引导下独立完成完整的 reverse solver，他预计在不久的将来，AI 可以 zero-shot 完成整个扑克求解器——也就是他整个博士论文的核心成果。

https://www.youtube.com/watch?v=AZrU6y3pUcU

---

Generated through the Follow Builders skill: https://github.com/zarazhangrui/follow-builders
