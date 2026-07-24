# 弄清楚职业处境 Skill

这是一个面向已有工作经历者的开源 AI Skill。它不做性格测试，而是通过行业、公司、部门和关系人“四张钱图”，帮助用户：

- 看清岗位为什么被付钱；
- 区分事实、推断、假设和待验证信息；
- 识别可交易能力、可携带资产和关键依赖；
- 比较留任、换岗、副业或创业等现实路径；
- 形成一个低风险、可验证的下一步行动。

## 当前状态

版本：v0.1，人工验证阶段。

现有流程已经可以帮助用户系统梳理和初步定位职业处境，但不能保证诊断绝对准确，也不能替用户决定辞职、转行或创业。重要结论必须由用户核对，并通过真实数据或行动继续验证。

## 最简单的使用方式

把 [`skills/diagnose-career-situation`](skills/diagnose-career-situation) 整个文件夹安装到支持 `SKILL.md` 的 AI Agent，然后说：

> 帮我梳理当前职业处境。我会提供真实工作案例，请区分事实、推断、假设和待验证项，并给我一个7天内能执行的行动。

用户也可以先填写 [`intake-form.md`](skills/diagnose-career-situation/assets/intake-form.md)，再交给 AI 分析。

## 文件结构

```text
skills/diagnose-career-situation/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── interview-guide.md
│   ├── evidence-and-reasoning.md
│   └── report-template.md
└── assets/
    └── intake-form.md
```

核心 `SKILL.md` 只保留执行流程。访谈、证据规则和报告模板由 Agent 在需要时读取，避免一次加载过多内容。

## 安装到 Codex

下载本仓库后，将 `skills/diagnose-career-situation` 文件夹复制到：

```text
%USERPROFILE%\.codex\skills\
```

重新打开 Codex 后，可以用 `$diagnose-career-situation` 明确调用。

不同 Agent 对 Skill 的目录和安装方式可能不同，请以相应产品的当前说明为准。

## 上传到小红书 RED Skill

1. 登录小红书 PC 端创作服务平台。
2. 进入 `Builder Hub` 或 `RED Skill`。
3. 选择上传原创 Skill。
4. 上传 `skills/diagnose-career-situation` 文件夹或压缩包；如果界面只允许单文件，先上传 `SKILL.md`，并根据平台提示补充引用文件。
5. 填写名称、简介、使用场景、权限和数据用途，提交审核。
6. 审核通过后，在发布笔记时选择“添加组件”，挂载该 Skill。

平台界面和支持格式可能变化，应以账号后台显示为准。

## 隐私与边界

- 不要求用户提供公司名称、客户名称、账号密码或商业机密。
- 金额可以使用区间。
- 不提供心理诊断、法律意见、投资建议或结果保证。
- 缺少现金流和风险承受信息时，不建议辞职、借贷或大额投入。
- 公开案例前必须获得授权并彻底匿名化。

## 建议如何验证

首轮不要只看点赞或安装次数。至少记录：

- 完成诊断人数；
- 用户认为准确和不准确的判断；
- 7天内执行行动的人数；
- 愿意推荐的人数；
- 愿意为完整诊断付费的人数。

## 开源许可

本项目采用 MIT License。你可以使用、修改和再发布，但需要保留版权和许可声明。
# career-situation-skill
用四张钱图梳理职业处境、能力证据、利益关系与下一步行动的开源 AI Skill
