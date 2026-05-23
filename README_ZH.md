# 庄的配图创作 Master

Zhuang Infochart Master 是一个面向 GPT Image 2 的 Agent Skill，用来生成知识型配图。

你可以给它一段很自然、甚至有点零散的需求：一组数据、一个流程、一段方法论、一个想解释的概念。它会帮 Agent 判断内容类型，推荐视觉风格，写出可直接作图的英文 Prompt，同时给一版中文理解说明。用户确认后，它可以调用 Agent 自带的生图能力，也可以用内置脚本走 fal.ai API。

它不是泛泛的“帮我画张图”。它主要服务文章配图、知识解释图、流程图、数据图表和轻量信息图。

## 能做什么

- 数据图表：KPI 汇报、采用率、调查分布、进度、状态和业务指标。
- 流程图：SOP、服务流程、onboarding、AI Agent 链路、审核闭环。
- 概念解释：框架卡片、产品概念、AI 术语、课程讲义里的概念图。

当前内置风格：

| 内容类型 | 风格流派 |
| --- | --- |
| 数据图表 | WebUI Clean Modern、Isometric Creative、Ink Minimal |
| 流程图 | WebUI Clean Modern、Notion Handdrawn、Ink Minimal、Isometric Creative |
| 概念解释 | WebUI Cards、Ink Minimal |

## 示例图

下面这些图来自批量测试。每个示例都附了原始作图 Prompt，方便你判断这个 Skill 的实际产出边界。

### 数据图表

#### WebUI Clean Modern

干净的 SaaS 汇报页风格，适合 KPI、增长、转化、预算、进度等业务数据。

![WebUI Clean Modern](https://i.ibb.co/Vc7d7nym/data-webui.png)

<details>
<summary>原始作图 Prompt</summary>

```text
Create a clean modern SaaS business report slide for an internal weekly meeting, designed to be shared in Notion and a Feishu group. Use a 16:9 horizontal canvas with a white or very light gray background, generous whitespace, strict alignment, flat vector styling, clean vector edges, subtle grid lines, modern sans-serif typography, black and soft gray base colors, and one vivid blue accent color.

Composition: build a polished Web UI style data visualization slide, not a traditional Excel chart. Place the large bold title "AI Sales Assistant Lift" at the top left. Make the main visual focus a rounded vertical bar chart titled "Q3 MRR Growth" showing three monthly MRR bars with exact labels: "Jul $124K", "Aug $158K", "Sep $196K". The bars should grow clearly from July to September, with the September bar dominant in blue and the earlier bars in softer blue or gray-blue. Keep the chart minimal, spacious, and easy to read.

On the right side, create three compact KPI cards with rounded corners and subtle shadows. Each KPI card should show one concise before-to-after improvement: "Lead Response Time" with "18h to 5.5h"; "Trial to Paid" with "6.8% to 9.5%"; "Customer Churn" with "4.2% to 2.7%". Use small directional micro-indicators such as a downward arrow for response time and churn, and an upward arrow for conversion, but do not add any extra explanatory text.

At the bottom right, include the source line "Internal CRM + Billing Review, Q3 2026". Keep all visible text sparse, crisp, and readable at social-sharing size. Use rounded bars, rounded cards, subtle dividers, balanced margins, and a restrained SaaS report aesthetic.

no complex dashboard, no app sidebar, no navigation bar, no filters, no dense table, no isometric, no 3D, no photo, no characters, no rainbow palette, no heavy decoration, no clutter, no tiny unreadable text, no fake labels, no watermark, no logos.
```
</details>

#### Isometric Creative

2.5D 数据小景观，适合对比、分布、趋势和需要传播感的数据洞察。

![Isometric Creative](https://i.ibb.co/9HXR2hqZ/data-isometric.png)

<details>
<summary>原始作图 Prompt</summary>

```text
Create a 16:9 horizontal editorial isometric data insight infographic for a WeChat article.

Use a miniature isometric data landscape on a warm off-white paper-like background with a very subtle light-gray isometric grid floor. The image should feel like a premium data-news illustration and high-end business report: crisp vector-like edges, flat muted colors, dark charcoal side faces on the objects, subtle grounding shadows, clean spacious composition, not a dashboard and not a generic PowerPoint chart.

Visible text must be sparse, large, and readable. Include only these exact text elements, with no extra words:
"Agent Adoption by Function"
"客服" "82%"
"销售" "76%"
"内容团队" "68%"
"产品" "54%"
"财务" "31%"
"法务" "18%"
"Internal Enablement Survey, May 2026"

Place the large elegant high-contrast black serif title "Agent Adoption by Function" in the upper-left. Place the source "Internal Enablement Survey, May 2026" small and quiet near the lower-left or lower-right edge.

Transform the six AI Agent adoption rates into proportional physical isometric objects, like a miniature city district made of extruded percentage numbers, plinths, and tower-like platforms. Make "客服" at "82%" the dominant right-side visual anchor: the tallest, most confident platform, with a large extruded "82%" on top and a clean standing placard labeled "客服". Put "销售" at "76%" close beside it as the second-tallest leading platform, visually paired with customer service to show that these two functions are clearly ahead. Use confident but muted accent colors for these two leading districts, such as teal and deep blue.

Arrange "内容团队" at "68%" and "产品" at "54%" across the middle-left area in a balanced diagonal rhythm, with medium-height platforms that are clearly readable but subordinate to the top two. Place "财务" at "31%" and "法务" at "18%" as smaller, lower, more cautious platforms toward the lower-left foreground, using quieter muted colors and more compact geometry to suggest conservative adoption without adding explanatory labels.

Scale every platform, tower, and extruded percentage number proportionally to its value. Use tiny pedestrians, simple trees, and small geometric props only as secondary scale cues. Keep each department label and percentage value visually connected to its own platform. Maintain generous whitespace around the title and prevent all labels from overlapping.

Negative constraints: no legends, no axes, no explanatory paragraphs, no extra annotations, no unrelated icons, no photorealism, no glossy 3D render, no futuristic dashboard UI, no neon glow, no gradients dominating the image, no heavy shadows, no clutter, no distorted text, no misspelled labels, no additional data, no watermark, no logos.
```
</details>

#### Ink Minimal

黑白灰研究报告风，适合调查结果、进度、状态分布和运营指标。

![Ink Minimal](https://i.ibb.co/FLKkRzfb/data-ink.png)

<details>
<summary>原始作图 Prompt</summary>

```text
Create a 16:9 horizontal monochrome ink data visualization that looks like one restrained page from a printed technical research report, not a dashboard.

Use a warm off-white or neutral light gray paper background, black ink linework, thin outlines, subtle pale gray grid lines, strict alignment, generous whitespace, and clean monospaced or modern sans-serif typography. The visual language should feel like an editorial research note or technical report figure.

Main composition: a centered report-page layout with the title at the upper left, a quiet subtitle underneath, and one dominant horizontal stacked survey bar across the middle. The stacked bar shows five maturity stages in order from least mature to most automated. Use distinct monochrome fills for each segment: white outlined fill, light gray fill, diagonal hatch, dense hatch, and solid black. Put the percentage inside or directly above each segment in large readable numerals. Place each stage label beneath its segment, aligned to the segment center, with enough spacing to stay legible.

Add a small quiet right-side annotation block using only thin black rules and gray text hierarchy to emphasize that agent automation is still rare, without adding extra data. Keep the page calm, analytical, and sparse.

Visible text must be limited to these exact strings, rendered verbatim in straight double quotes:
"Editorial AI Workflow Maturity"
"Beyond trial, not yet automated"
"Fully manual"
"12%"
"AI research only"
"23%"
"AI drafts first version"
"29%"
"Fixed Prompt SOP"
"24%"
"Agent-orchestrated automation"
"12%"
"Agent automation remains rare"
"Team Survey, n=42, 2026"

Make all text crisp, correctly spelled, and readable. Keep the data values exact. Do not add legends, navigation, filters, extra section headings, explanatory paragraphs, logos, or any invented numbers.

No colorful SaaS dashboard, no blue-violet accent system, no rainbow palette, no neon glow, no gradient background, no glassmorphism, no heavy drop shadows, no 3D, no isometric perspective, no extruded chart objects, no photorealism, no people, no decorative illustration, no complex BI dashboard, no navigation, no filters, no dense table, no tiny unreadable labels, no fake text, no misspelled labels, no invented data, no watermark, no logos.
```
</details>

### 流程图

#### WebUI Clean Modern

现代 SaaS 流程卡片，适合工作流、SOP、onboarding 和产品文档。

![WebUI Clean Modern](https://i.ibb.co/8LB1Vwgd/flow-webui.png)

<details>
<summary>原始作图 Prompt</summary>

```text
Create a 16:9 horizontal image for a SaaS product explanation page: a clean modern Web UI / pitch deck process diagram titled "AI QA Feedback Loop". The diagram explains an AI customer service QA feedback loop for customer experience operations leaders.

Use a white or very light gray background with subtle grid lines, generous whitespace, strict alignment, modern sans-serif typography, thin dividers, rounded step cards, light shadows, and one vivid blue accent color. Use a simple horizontal five-step workflow with clear connector arrows from left to right, plus a subtle final curved arrow or loop cue from step 05 back toward the beginning to suggest continuous weekly improvement. Keep the design elegant and readable, like a SaaS website "how it works" section, not an architecture diagram.

Only include these visible text strings, rendered verbatim in straight English double quotes:
"AI QA Feedback Loop"
"01"
"Import Customer Conversations"
"02"
"AI Tags Risk Points"
"03"
"Supervisor Sample Review"
"04"
"Push Issues to Agents"
"05"
"Review Next-Week Trends"
"Source: CX Operations Playbook, 2026"

For each step card, use a simple line icon or tiny UI motif that matches the step: conversation import, AI risk tagging, supervisor review, agent feedback push, and trend review. Keep icons secondary to the text. Make the step sequence visually obvious and uncluttered, with no extra explanatory copy.

Negative constraints: no complex dashboard, no app sidebar, no navigation bar, no filters, no dense table, no isometric, no 3D, no photo, no characters, no rainbow palette, no heavy decoration, no clutter, no tiny unreadable text, no fake labels, no invented steps, no watermark, no logos.
```
</details>

#### Notion Handdrawn

轻量手绘说明图，适合课程、文章、轻教程和友好型流程解释。

![Notion Handdrawn](https://i.ibb.co/yFhwmH8F/flow-notion.png)

<details>
<summary>原始作图 Prompt</summary>

```text
Create a 16:9 information visual in the chosen layout: Horizontal Process Row. Minimal black-and-white Notion-style hand-drawn process diagram on a pure white background, designed for a course document rather than a commercial landing page.

Place the exact title "From Interview to Article" at the top center in clean, readable sans-serif type with a slight hand-drawn looseness. Under the title, arrange five evenly spaced steps from left to right, connected by thin hand-drawn arrows. Keep generous white space around every step.

Each step should have a small numbered label and one simple black line-art illustration:

1. Visible label: "1 Upload". Illustration: a simple audio file icon and transcript page being dropped into an upload tray.
2. Visible label: "2 Extract". Illustration: a small AI sparkle or simple assistant mark pulling quote bubbles and a story thread line from the transcript.
3. Visible label: "3 Choose Thread". Illustration: an editor figure circling one path among three loose story lines.
4. Visible label: "4 Draft". Illustration: a document page transforming into a WeChat-style article draft page, with only a few generic text lines.
5. Visible label: "5 Polish & Publish". Illustration: a human hand adding a title line, a small image placeholder, and a publish check mark.

Use thin black outlines, slight imperfect hand-drawn strokes, tiny annotation dots, simple human figures where useful, and very light gray shadow only if needed for separation. Keep all visible text sparse, large enough to read, and exactly as quoted. Make the diagram feel like a friendly Notion note illustration or hand-drawn classroom explainer.

Negative constraints: no colorful infographic, no corporate dashboard, no backend system UI, no admin panels, no complex architecture diagram, no 3D, no isometric view, no photorealism, no glossy gradients, no dense text, no tiny unreadable labels, no icons that look like enterprise software, no heavy borders, no dark background.
```
</details>

#### Ink Minimal

黑白 SOP 技术手册风，适合审核链、安全检查和运营执行链路。

![Ink Minimal](https://i.ibb.co/j9ZvLhKj/flow-ink.png)

<details>
<summary>原始作图 Prompt</summary>

```text
Create a 16:9 horizontal minimal monochrome ink process diagram for an internal standards document. The image should look like a printed technical manual SOP sheet, not a colorful product page.

Use a warm off-white or neutral light gray paper background with subtle pale gray grid lines, black ink linework, thin outlined boxes, strict alignment, generous whitespace, monospaced or clean modern sans-serif typography, and almost no shadows. Build a left-to-right numbered process rail with five rectangular step nodes connected by thin black arrows. Make the transformation obvious: raw draft intake -> automated risk scan -> editor confirmation -> legal review of flagged excerpts -> approved publishing schedule.

Only include these visible text strings, rendered verbatim in straight English double quotes:
"Pre-Publish AI Safety Check"
"1"
"Raw Draft Intake"
"Enters pending review queue"
"2"
"Model Risk Scan"
"Facts • sensitive wording • copyright"
"3"
"Editor Confirmation"
"High-risk passages verified"
"4"
"Legal Review"
"Flagged excerpts only"
"5"
"Schedule for Publishing"
"Approved content enters calendar"

For step 2, show three small black-outline check modules inside the node, but do not add extra labels beyond the allowed text. For step 3, show a small editor check mark and a document excerpt marker. For step 4, represent the user's "red-marked fragments" concept without using red: use black hatch highlight bars and a narrow review gate that visually filters only the flagged excerpt strips into the legal node. For step 5, show a simple calendar outline as the final destination. Keep all captions large enough to read.

Strong negative constraints: no colorful SaaS dashboard, no blue-violet accent system, no rainbow palette, no neon glow, no gradient background, no glassmorphism, no heavy drop shadows, no 3D, no isometric perspective, no photorealism, no people, no decorative illustration, no complex BI dashboard, no BPMN diagram, no system architecture diagram, no dense table, no tiny unreadable labels, no fake text, no misspelled labels, no invented steps, no watermark, no logos.
```
</details>

#### Isometric Creative

2.5D 服务旅程图，适合客户交付流程和更有视觉记忆点的流程故事。

![Isometric Creative](https://i.ibb.co/PZDvRG3b/flow-isometric.png)

<details>
<summary>原始作图 Prompt</summary>

```text
Create a 16:9 horizontal information visual for a proposal PDF titled "Knowledge Base Build Journey".

Show a miniature isometric process landscape on a warm off-white paper-like background with a subtle light-gray isometric grid floor. The subject is a service delivery journey for building an enterprise knowledge base for a client, designed for potential customers and sales teams. Use crisp vector-like edges, flat muted colors, dark charcoal side faces, subtle isometric grounding shadows, and a polished B2B consulting / SaaS proposal feel.

Use a diagonal process landscape that begins at the lower left and ends at the upper right. Connect six miniature isometric stations with one continuous visible path, arrow ribbon, small bridge segments, or track, so the viewer feels they are walking step by step through the journey. Keep the composition spacious and readable at PDF scale.

Place the title "Knowledge Base Build Journey" prominently at the top. Each station has exactly one nearby readable label:

1. "需求访谈" — an isometric consultation table with two business people, a notebook, and simple speech-bubble shapes, showing requirements discovery.
2. "资料收集" — organized folders, document stacks, cloud-drive boxes, and files being gathered into a tray.
3. "清洗与切分" — documents passing through a clean filtering and cutting workstation, with neat knowledge chunks arranged as small cards.
4. "搭建检索和评测" — a compact search console, magnifier, index blocks, and checklist score panel, showing retrieval setup and evaluation.
5. "试运行" — a small pilot workspace where users test a knowledge search box, with feedback pins and a simple progress marker.
6. "交付培训" — a presentation screen, trainer, audience seats, and a completed knowledge-base cube being handed over.

Visible text must be limited to the exact title "Knowledge Base Build Journey" and the six step labels "需求访谈", "资料收集", "清洗与切分", "搭建检索和评测", "试运行", "交付培训". Do not add captions, paragraph text, legends, UI copy, source notes, logos, or decorative pseudo-text.

Negative constraints: no dashboard UI, no flat generic flowchart, no BPMN diagram, no system architecture diagram, no glossy 3D render, no photorealism, no neon glow, no heavy gradients, no clutter, no tiny unreadable text, no distorted text, no misspelled labels, no invented steps, no watermark, no logos.
```
</details>

### 概念解释

#### WebUI Cards

渐变 Web UI 概念卡片，适合产品概念、AI 术语、功能模块和知识卡片。

![WebUI Cards](https://i.ibb.co/qF3gWr92/concept-cards.png)

<details>
<summary>原始作图 Prompt</summary>

```text
Create a polished 16:9 article illustration for product managers explaining the concept of "Context Engineering" as something broader than prompt engineering.

Composition: a light, modern SaaS-style canvas with the large title "Context Engineering" at the top, a small subtitle "Beyond prompt engineering", and four clean white rounded Web UI cards arranged in a balanced 2x2 grid. Use generous whitespace, soft low-contrast shadows, thin light borders, modern readable sans-serif typography, pastel gradient illustration areas, and subtle blurred glowing color blobs on a warm off-white background.

Card 1 visible title: "Right Background". Short visible line: "Relevant docs, facts, examples". Micro-UI motif: a compact document stack feeding an abstract model input panel, with tiny highlighted placeholder bars and a soft blue-to-lavender gradient.

Card 2 visible title: "Tool Boundaries". Short visible line: "Clear permissions and limits". Micro-UI motif: a simple abstract tool-call panel with a boundary frame, icon-only permission chips, and one muted blocked icon, using peach and pale yellow accents.

Card 3 visible title: "User State & Memory". Short visible line: "Current state plus history". Micro-UI motif: a small abstract profile/state card connected to a memory timeline, with placeholder message bubbles and soft pink-to-lavender gradients.

Card 4 visible title: "Eval Feedback". Short visible line: "Tests improve the loop". Micro-UI motif: a lightweight evaluation loop with icon-only score chips, a tiny progress bar, and a feedback arrow returning to the system, using pale blue and mint accents.

Every card illustration must be derived from its own concept meaning, action, object, and outcome. Keep all visible text sparse, crisp, and readable. Use only the exact visible text strings listed above: "Context Engineering", "Beyond prompt engineering", "Right Background", "Relevant docs, facts, examples", "Tool Boundaries", "Clear permissions and limits", "User State & Memory", "Current state plus history", "Eval Feedback", "Tests improve the loop". Inside micro-UI motifs, use icons, placeholder bars, dots, chips, and abstract shapes only; do not render any extra UI words, numbers, scores, names, labels, menu items, actions, or annotations. The result should feel like premium Web UI concept cards for a thoughtful product article, not a dashboard.

Negative constraints: no complex dashboard, no real webpage screenshot, no app sidebar, no navigation bar, no dense table, no long paragraphs, no generic unrelated icons, no random decorative symbols, no dark theme, no neon cyberpunk, no heavy 3D, no realistic photo, no characters, no clutter, no tiny unreadable text, no extra text beyond the listed visible strings, no fake labels, no watermark, no logos.
```
</details>

#### Ink Minimal

黑白技术概念卡片，适合框架、模型、方法论和课程讲义。

![Ink Minimal](https://i.ibb.co/Gv0mj9mL/concept-ink.png)

<details>
<summary>原始作图 Prompt</summary>

```text
An Ink Minimal concept explanation card illustration for a serious article and course handout, 16:9 horizontal format on warm off-white paper. Create a black-and-white technical research-note composition with strict alignment, thin black bordered cards, subtle gray divider lines, generous whitespace, small monochrome ink line icons, tag chips, index numbers, connector lines, and very light hatch fills.

Composition: place the exact title "Agent Memory Operating System" across the top in clean sans-serif or monospaced typography. Under the title, create a central thin-bordered system box labeled "Memory OS" with a small circular mechanism diagram inside it. Around the central box, arrange four thin-bordered component cards in a balanced 2x2 grid:

1. Card title "Short-Term Context"; short definition "What the agent is using right now."; tags "session", "task state", "working set"; icon: a small open notebook with a clock mark.
2. Card title "Long-Term Fact Store"; short definition "Stable facts kept across sessions."; tags "profile", "facts", "history"; icon: a small archive drawer with labeled index tabs.
3. Card title "Retrieval Routing"; short definition "Find the right memory before answering."; tags "query", "rank", "route"; icon: a forked path with a magnifying glass.
4. Card title "Write Rules"; short definition "Decide what deserves to be saved or changed."; tags "criteria", "provenance", "update"; icon: a checklist beside a pencil.

In the central mechanism diagram, show a simple circular loop with four exact labels: "Read", "Judge", "Write", "Update". Use thin arrows to connect the loop to the four component cards. Add one small caption below the central system box: "Not random remembering; a governed memory mechanism." Keep all text short, large enough to read, and unobstructed.

Visual hierarchy: title first, central mechanism second, four components third. Use only black ink, soft gray, and off-white paper. Make the card feel like a polished black-and-white research note or technical concept card from a course lecture, not a product dashboard. Require precise layout, crisp linework, readable typography, and no invented labels beyond the quoted visible text.

Negative constraints: no colorful SaaS cards, no pastel gradients, no glowing blobs, no dashboard, no KPI charts, no data-first chart layout, no 3D, no isometric perspective, no photorealism, no people, no decorative illustration, no dense table, no long paragraphs, no fake text, no random English, no misspelled text, no watermark, no logos.
```
</details>


## 从 GitHub 安装

克隆仓库，然后把 Skill 文件夹复制到你的 Agent 技能目录。

```bash
git clone https://github.com/billzhuang6569/zhuang-infochart-master.git
mkdir -p ~/.codex/skills
cp -R zhuang-infochart-master/skills/zhuang-infochart-master ~/.codex/skills/
```

如果你的 Agent 使用的是其他技能目录，把 `skills/zhuang-infochart-master` 复制到对应目录即可。

仓库里的 `config.json` 默认不包含 API key。如果你要使用 fal.ai 兜底生图或改图，请在本地填写自己的 key。不要把 key 提交到 GitHub。

## For AI AGENT

你可以用两种方式安装这个 Skill。

### 方式一：直接通过本仓库安装

1. 克隆这个仓库。
2. 将 `skills/zhuang-infochart-master` 复制到当前 Agent 的技能目录。
3. 检查安装目录下是否存在 `SKILL.md`。
4. 如果用户需要用 fal.ai 生图或改图，请提醒用户在本地填写 `config.json`。
5. 如果当前环境只在启动时加载技能，请提醒用户重启或重新加载 Agent。

可直接给 Agent 的提示词：

```text
请从这个 GitHub 仓库安装 Agent Skill：
https://github.com/billzhuang6569/zhuang-infochart-master

把 skills/zhuang-infochart-master 复制到当前环境的技能目录。安装后检查 SKILL.md 是否存在。不要编造 API key；如果需要通过 fal.ai 生图，请提醒我在本地填写 config.json。
```

### 方式二：通过小庄Sir的 SKILLHUB 安装

SKILLHUB 地址：https://skills.woe.show/

目标 Skill：

```text
zhuang-infochart-master
Record_ID：recvkqMwmkJzhh
```

可直接给 Agent 的安装提示词：

```text
# 任务目标
确保用户环境中正确安装并更新 woe-skill-share Skill，
然后使用该 Skill 下载并安装指定的目标Agent SKILL。

# Workflow
步骤 1：检测并安装 woe-skill-share
- 检查是否已安装 woe-skill-share Skill。
- 确认当前版本是否为 1.1.1。
- 若未安装或版本不匹配，则执行以下命令以下载并安装最新版本：
curl -X POST "https://n8n.whatonearth.work/webhook/ba39d4a7-18db-4731-9854-af1e540ce9ac-download?record_id=recvgv3fii1Lzk&agent=website"

成功安装后提示用户：
✅ woe-skill-share Skill 已成功更新至最新版本（1.1.1）。

步骤 2：使用 woe-skill-share 下载目标 Skill
- 使用该 Skill 调用其“下载技能”功能，从 WOE（WhatOnEarth）下载目标 Skill。
- 下载参数：
Record_ID：recvkqMwmkJzhh

成功获取后，自动解压并安装 Skill，并反馈安装状态。
```

## 兜底生图和改图

优先使用当前 Agent 自带的生图能力。如果 Agent 不能直接生图，或者无法把图片保存到 run 目录，可以使用内置脚本。

文生图：

```bash
python3 scripts/render_image.py --mode create --prompt-file runs/example/final_prompt_en.txt --run-dir runs/example --channel fal
```

改图：

```bash
python3 scripts/render_image.py --mode edit --prompt-file runs/example/final_prompt_en.txt --image-url https://example.com/source.png --run-dir runs/example --channel fal
```

