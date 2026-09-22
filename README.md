# problem-definition

> 把“我觉得不对”还原成“到底发生了什么”，再决定要不要行动。

problem-definition 是一个问题界定工具箱：把感受、评价和模糊描述转成可核实的事实、边界、原因和差距。它适合 DeepWorks、OpenCode、Claude Code 等支持 `SKILL.md` 的 Agent。

---

## 它真正在解决什么

问题经常在还没被定义清楚之前，就被拿去开会、拆任务和找方案：

- “项目推进很慢”到底慢在哪里，谁观察到的，慢了多少；
- “大家都不配合”是行为事实，还是对行为的评价；
- 一段汇报里哪些是原始事实，哪些是转述、推断和情绪；
- “要不要换方案”背后真正要解决的目标、现状和差距是什么。

这个 skill 的原则只有一句：**先界定，再分析；先核实，再决策。**

## 它和直接要方案有什么不同

| 直接要方案 | problem-definition |
|---|---|
| 把感受当成问题本身 | 先把感受还原为对象、行为、时间和数字 |
| 用猜测填补材料缺口 | 缺数据标“待确认”，推测标“待核实” |
| 只给一个听起来可行的解释 | 区分事实、评价、假设和证据，并保留出处 |
| 方案越多越显得完整 | 先找到尚未闭环的那一环，再决定是否需要方案 |

它不负责替你拍板，而是让拍板时面对的是同一个问题。

## 八个方法

| 方法 | 用来做什么 |
|---|---|
| 问题分型 | 区分发生型、潜在型和理想型问题，避免动作错配 |
| 还原事实 | 把“很乱、太慢、不配合”改写成可核实的事实 |
| 筛事实 | 从汇报、邮件和转述中筛出事实与加工痕迹 |
| 5W2H 补边界 | 补齐对象、时间、地点、范围、原因和承诺依据 |
| 5 Why 追原因 | 追到第一个只能靠猜的环节，并在那里停住 |
| 假设反证 | 检查假设、反证和补救方案的“承重墙” |
| 目标-现状-差距 | 把模糊决策句改写成可验证的差距 |
| 向上沟通 | 输出三行同步、追问预案和汇报前准备清单 |

## 四种使用方式

| 方式 | 适用场景 |
|---|---|
| 单点取用（默认） | 你只想筛一段事实、补一次边界或做一次 5 Why |
| 完整界定 | 从问题分型一路走到目标-现状-差距 |
| AI 推荐 | 只有一段模糊描述，不知道从哪个方法切入 |
| 二次界定 | 已经有初稿，只补新增信息，不重复跑完整流程 |

## 三条底线

1. **不编造**：缺数据就写“待确认”。
2. **推测必标注**：AI 推断统一写“待核实”。
3. **事实带出处**：没有出处的内容只能算印象，不能当结论。

## 安装

全局安装：

~~~bash
git clone https://github.com/guangquan123/problem-definition ~/.agents/skills/problem-definition
~~~

项目级安装：

~~~bash
git clone https://github.com/guangquan123/problem-definition .opencode/skills/problem-definition
~~~

Claude Code：

~~~bash
git clone https://github.com/guangquan123/problem-definition ~/.claude/skills/problem-definition
~~~

## 第一次跑

在 Agent 中说：

~~~text
初始化 problem-definition
~~~

也可以直接把一段模糊描述交给它：

~~~text
最近团队氛围很怪，我说不上来哪里不对。
~~~

## 日常用法

~~~text
“帮我把‘项目推进很慢’改写成可核实的问题。”
“筛一下这段转述里哪些是真的，哪些是评价。”
“用 5 Why 找到第一个没有证据的环节。”
“把目标、现状和差距整理成一页。”
“帮我准备向上汇报和可能被追问的问题。”
~~~

## 仓库内容

~~~text
problem-definition/
├── SKILL.md
├── references/
│   ├── fact-filtering.md
│   └── upward-report.md
└── templates/
    └── report-template.md
~~~

它可以独立使用，也可以和 [problem-analysis](https://github.com/guangquan123/problem-analysis) 接力：先锁定真问题，再拆解、验证和决策。

## License

[MIT](./LICENSE)
