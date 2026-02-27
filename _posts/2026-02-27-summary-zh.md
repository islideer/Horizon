---
layout: default
title: "Horizon Summary: 2026-02-27 (ZH)"
date: 2026-02-27
lang: zh
---

> From 29 items, 9 important content pieces were selected

---

1. [Anthropic 面临五角大楼压力要求提供 AI 用于军事用途，面临《国防生产法》被援引的风险](#item-1) ⭐️ 9.0/10
2. [vLLM v0.16.0 发布，引入异步调度、实时 API 及重大 XPU 平台更新](#item-2) ⭐️ 8.0/10
3. [Andrej Karpathy 宣称 AI 编程智能体在 2025 年 12 月取得突破](#item-3) ⭐️ 8.0/10
4. [Google Maps API 密钥在启用 Gemini 后变为危险的 Gemini 密钥](#item-4) ⭐️ 8.0/10
5. [美国国防部向 Anthropic 下达最后通牒，要求解除 Claude AI 模型安全限制](#item-5) ⭐️ 8.0/10
6. [tldraw 测试套件迁移引发关于 AI 对开源威胁的讨论](#item-6) ⭐️ 7.0/10
7. [开发者一夜之间使用 vibe coding 为 LLM 演讲创建自定义 macOS 演示应用](#item-7) ⭐️ 7.0/10
8. [连接标准联盟发布 Aliro 1.0 规范，统一移动访问控制标准](#item-8) ⭐️ 7.0/10
9. [逾 200 名 Google 与 OpenAI 员工联署声援 Anthropic 限制军事与监控用途](#item-9) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Anthropic 面临五角大楼压力要求提供 AI 用于军事用途，面临《国防生产法》被援引的风险](https://www.anthropic.com/news/statement-department-of-war) ⭐️ 9.0/10

Anthropic CEO Dario Amodei 透露，美国国防部正施压该公司，要求其提供 AI 模型用于无限制的军事用途，并威胁称如果拒绝，将援引《国防生产法》并将 Anthropic 指定为'供应链风险'。五角大楼要求 Anthropic 在周五下午 5 点前满足其要求。 这场冲突是 AI 伦理在实践中的一次关键考验，使企业原则与国家安全需求形成对立，并可能为其他 AI 公司如何被对待开创先例。其结果可能决定 AI 开发者在面临政府要求军事应用的施压时，能否守住伦理红线。 五角大楼的威胁包括援引《国防生产法》强制 Anthropic 满足军事需求，以及将该公司标记为供应链风险，这将迫使军事承包商停止与 Anthropic 的业务往来。这种施压发生在 Anthropic 自 2025 年 7 月起已与国防部首席数字和人工智能办公室达成 2 亿美元协议的情况下。

hackernews · qwertox · Feb 26, 22:42

**背景**: 《国防生产法》是一项 1950 年通过的法律，赋予联邦政府广泛的权力，可以指示私营公司满足国防需求。'供应链风险'指定是一个严重的标签，可以有效地将一家公司列入国防承包黑名单。Anthropic 是一家以开发 Claude AI 模型而闻名的 AI 安全公司，一直将自己定位为致力于有伦理边界的负责任 AI 开发。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://federalnewsnetwork.com/defense-news/2026/02/what-to-know-about-defense-protection-act-and-the-pentagons-anthropic-ultimatum/">What to know about the Defense Production Act and the ...</a></li>
<li><a href="https://www.msn.com/en-in/technology/artificial-intelligence/pentagon-may-designate-anthropic-as-supply-chain-risk-what-this-means-for-the-company-its-customers-and-partners/ar-AA1Ww0ev">Pentagon may designate Anthropic as ' supply chain risk ': What this...</a></li>
<li><a href="https://www.cbsnews.com/news/pentagon-anthropic-offer-ai-unrestricted-military-use-sources/">DoD officials sent Anthropic final offer for military use of ...</a></li>

</ul>
</details>

**社区讨论**: 社区讨论显示出不同的反应，一些人赞赏 Anthropic 的原则立场，而另一些人则基于该公司过去的行动质疑其一致性。一位评论者指出，Amodei 的声明批评了 AI 驱动的国内大规模监控，但并未明确谴责部分自主监控或未来使用的完全自主武器，这引发了人们对潜在漏洞的担忧。

**标签**: `#AI Ethics`, `#Government Regulation`, `#Corporate Responsibility`, `#Military AI`, `#AI Safety`

---

<a id="item-2"></a>
## [vLLM v0.16.0 发布，引入异步调度、实时 API 及重大 XPU 平台更新](https://github.com/vllm-project/vllm/releases/tag/v0.16.0) ⭐️ 8.0/10

vLLM v0.16.0 正式引入了异步调度与流水线并行支持，带来了超过 30% 的吞吐量提升，并推出了一个基于 WebSocket 的实时 API 用于流式音频交互。此次发布还包括对 RLHF 工作流的重大改进，以及对 XPU 平台的全面重构，用 vllm-xpu-kernels 取代了 IPEX，并增加了广泛的新内核支持。 此次发布显著提升了大规模语言模型推理的效率和可扩展性，使其对于高需求的生产部署更具成本效益。新的实时 API 为语音驱动的 AI 智能体应用打开了大门，而对 XPU 平台的重构则扩展了硬件支持，使 vLLM 能在更多计算平台上发挥作用。 异步调度与流水线并行实现了 30.8% 的端到端吞吐量提升和 31.8% 的每输出令牌时间（TPOT）提升。该版本还引入了用于推测解码的“统一并行草稿生成”功能，允许在单次前向传播中并行生成多个草稿令牌以降低延迟。

github · khluu · Feb 25, 19:58

**背景**: vLLM 是一个用于大规模语言模型（LLM）的高吞吐、内存高效的推理和服务引擎。流水线并行是一种将模型拆分到多个 GPU 或节点上的技术，模型的不同层在不同设备上顺序处理，从而能够运行无法在单个 GPU 上容纳的更大模型。推测解码是一种推理加速技术，由一个更小、更快的“草稿”模型提出几个未来的令牌，然后由更大的目标模型并行验证，接受正确的预测以加速生成过程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/serving/parallelism_scaling/">Parallelism and Scaling - vLLM</a></li>
<li><a href="https://github.com/vllm-project/vllm/issues/11945">[RFC]: Pipeline-Parallelism for vLLM V1 #11945 - GitHub</a></li>
<li><a href="https://arxiv.org/html/2505.23219v1">Ghidorah: Fast LLM Inference on Edge with Speculative Decoding ...</a></li>

</ul>
</details>

**标签**: `#llm-inference`, `#high-performance-computing`, `#machine-learning`, `#parallel-computing`, `#ai-systems`

---

<a id="item-3"></a>
## [Andrej Karpathy 宣称 AI 编程智能体在 2025 年 12 月取得突破](https://simonwillison.net/2026/Feb/26/andrej-karpathy/#atom-everything) ⭐️ 8.0/10

知名 AI 研究员 Andrej Karpathy 指出，AI 编程智能体在 2025 年 12 月经历了一次显著且突然的突破，从基本无效转变为高度可用。他强调这一变化并非渐进式，而是一次明显的飞跃，现在的模型展现出更高的质量、长期连贯性和韧性，能够攻克大型、复杂的编程任务。 来自 AI 领域关键人物的这一观察，标志着软件开发可能到了一个转折点，AI 智能体通过自主处理更大、更复杂的编码项目，可能从根本上颠覆传统的编程工作流程。这预示着在不久的将来，开发者的生产力和软件工程工作的性质，可能会被能力强、有韧性的 AI 助手彻底改变。 Karpathy 指出这一突破存在'一些星号'或注意事项，尽管他在引文中未具体说明。核心改进在于模型增强的'长期连贯性'——在长时间任务中保持逻辑线索的能力——以及'韧性'，指的是它们能够坚持不懈地处理冗长、多步骤的问题而不会失败或丢失上下文。

rss · Simon Willison · Feb 26, 19:03

**背景**: AI 编程智能体是基于大型语言模型（LLMs）构建的 AI 系统，旨在协助或自主执行编程任务，如代码生成、调试和重构。'长期连贯性'对 AI 模型而言是一项具有挑战性的能力，指的是在长时间的交互或任务中保持一致性和逻辑推理的能力，这对于复杂的软件开发至关重要。此处的'韧性'描述的是 AI 能够坚持不懈地尝试并完成冗长、多步骤的任务，而不会放弃或偏离目标，这是实现实用编程辅助的关键要求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.lyzr.ai/glossaries/what-is-long-term-coherence/">Long term Coherence - lyzr.ai</a></li>
<li><a href="https://dev.to/brian_at_max_planck/the-reality-of-ai-in-programming-why-breaking-down-tasks-is-key-to-success-9lh">The Reality of AI in Programming: Why Breaking Down Tasks is Key to ...</a></li>

</ul>
</details>

**标签**: `#ai-assisted-programming`, `#coding-agents`, `#workflow-disruption`, `#andrej-karpathy`, `#llm-evolution`

---

<a id="item-4"></a>
## [Google Maps API 密钥在启用 Gemini 后变为危险的 Gemini 密钥](https://simonwillison.net/2026/Feb/26/google-api-keys/#atom-everything) ⭐️ 8.0/10

Truffle Security 的安全研究人员在 Google 的 API 密钥系统中发现了一个关键的权限提升漏洞。他们发现，当在同一 Google Cloud 项目中启用 Gemini 服务时，原本设计为嵌入网站、面向公众的 Google Maps API 密钥，会悄无声息地获得访问敏感且可计费的 Gemini AI API 端点的权限。 这一漏洞在开发者不知情的情况下，将原本无害的公开标识符转变为强大的秘密凭证，可能导致私人文件、缓存数据泄露，并允许攻击者利用受害者账户产生高额账单。它揭示了 Google Cloud 管理 API 密钥跨服务权限时存在的一个危险设计缺陷，影响了无数使用 Google Maps 并正在尝试 Gemini AI 的开发者。 Truffle Security 通过扫描 2025 年 11 月的网络数据，发现了 2,863 个可访问 Gemini 的已暴露 API 密钥，从而验证了该问题，其中甚至包括属于 Google 自身的密钥。一个关键的限制在于，新的 Google Cloud API 密钥默认被创建为“无限制”状态，授予其对项目中所有已启用 API 的访问权限，这就在添加像 Gemini 这样的新服务时埋下了固有风险。

rss · Simon Willison · Feb 26, 04:28

**背景**: Google Cloud API 密钥用于验证应用程序对 Maps、Gemini 等各种 Google 服务的访问权限。Google Maps API 密钥通常直接嵌入到公共网站的 HTML 或 JavaScript 中以加载地图，这使得它们本质上不是秘密。相比之下，Gemini API 密钥则需要保密，因为它们可以授权访问私有的 AI 模型交互、上传的用户文件，并产生使用费用。传统上，这些密钥是按服务管理的，但此漏洞揭示了一个共享的底层权限系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://trufflesecurity.com/blog/google-api-keys-werent-secrets-but-then-gemini-changed-the-rules">Google API Keys Weren't Secrets. But then Gemini Changed the Rules. Truffle Security Co.</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/previously-harmless-google-api-keys-now-expose-gemini-ai-data/">Previously harmless Google API keys now expose Gemini AI data - Bleeping Computer</a></li>
<li><a href="https://cybersecuritynews.com/google-api-keys-gemini/">Google API Keys Expose Private Data Silently Through Gemini</a></li>

</ul>
</details>

**标签**: `#security`, `#api-security`, `#google-cloud`, `#vulnerability`, `#devops`

---

<a id="item-5"></a>
## [美国国防部向 Anthropic 下达最后通牒，要求解除 Claude AI 模型安全限制](https://t.me/zaihuapd/39895) ⭐️ 8.0/10

美国国防部长皮特·赫格塞斯向 Anthropic 发出最后通牒，要求其在周五前取消其 Claude AI 模型的关键安全限制以供军方使用。五角大楼威胁称，如果 Anthropic 拒绝，将取消一份价值 2 亿美元的合同，并将其列为“供应链风险”。 这次对抗是 AI 安全原则与国家安全需求之间的一次关键考验，可能为政府如何强制 AI 公司修改其核心伦理护栏开创先例。其结果可能深刻影响先进 AI 在军事和监控领域的未来发展和部署，并冲击全球负责任 AI 使用的规范。 五角大楼特别威胁将动用《国防生产法》来强制其服从，这是一项通常用于国防紧急状态的法律。值得注意的是，Anthropic 此前已让 Claude 在安全级别达“秘密”级的 Palantir 平台上可用，这表明双方已存在一定程度的政府级合作。

telegram · zaihuapd · Feb 27, 02:18

**背景**: Anthropic 是一家以“宪法 AI”训练方法闻名的 AI 安全与研究公司，该方法将伦理原则直接嵌入其 Claude 等模型中。该公司以安全为先自我定位，并明确禁止其模型用于大规模监控或自主武器开发。《国防生产法》是一项美国法律，授予总统为国防利益指挥私营企业生产的广泛权力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theguardian.com/us-news/2026/feb/24/anthropic-claude-military-ai">US military leaders pressure Anthropic to bend Claude safeguards</a></li>
<li><a href="https://www.btimesonline.com/articles/176751/20260225/hegseth-gives-anthropic-72-hour-ultimatum-over-claude-ai-threatens-200-million-pentagon-contract.htm">Hegseth Gives Anthropic 72-Hour Ultimatum Over Claude AI, Threatens ...</a></li>
<li><a href="https://www.anthropic.com/">Home \ Anthropic</a></li>

</ul>
</details>

**标签**: `#AI Ethics`, `#Military AI`, `#Government Regulation`, `#AI Safety`, `#Anthropic`

---

<a id="item-6"></a>
## [tldraw 测试套件迁移引发关于 AI 对开源威胁的讨论](https://simonwillison.net/2026/Feb/25/closed-tests/#atom-everything) ⭐️ 7.0/10

tldraw 项目最初提议将其全面的测试套件迁移到私有仓库，理由是担心如此详细的测试可能使竞争对手能够利用 AI 工具从头开始重建其库。然而，项目维护者后来澄清该议题本意是个玩笑，并表示迁移测试会使开发复杂化，真正的价值在于产品决策，而不仅仅是代码。 这一事件突显了商业开源项目日益加剧的紧张关系：全面的测试套件虽然是保证质量的关键，但现在却可能成为 AI 智能体复制功能的详细规范，从而潜在地削弱项目的商业可行性。这反映了整个行业对 AI 辅助代码生成如何改变竞争格局，以及对混合了开放和封闭组件的软件的知识产权考量的广泛焦虑。 这场讨论直接受到了 Cloudflare 近期 'Vinext' 项目的启发，据报道，一名工程师利用 AI 在大约一周内将 Next.js 的大部分代码移植到 Vite，严重依赖了现有的测试套件。同样重要的是，tldraw 使用的是自定义许可证，要求在生产环境中使用需获得商业许可，这意味着它并非采用 MIT 或 Apache 等宽松许可证的传统开源项目。

rss · Simon Willison · Feb 25, 21:06

**背景**: tldraw 是一个用于构建无限画布和白板应用程序的流行软件开发工具包，以其实时协作功能和基于 React 的架构而闻名。测试套件是一组自动化测试的集合，用于验证软件应用程序的行为是否符合预期；在测试驱动开发中，这些测试可以有效地定义软件的规范。近期基于大语言模型的 AI 编码助手的进步，使得根据高级需求或详细测试用例生成功能代码成为可能，这引发了关于源代码本身保护价值的新问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/tldraw/tldraw">GitHub - tldraw/tldraw: very good whiteboard infinite canvas SDK</a></li>
<li><a href="https://www.theregister.com/2026/02/25/cloudflare_nextjs_api_ai/">Cloudflare vibe codes 94% of Next.js API 'in one week' • The Register</a></li>
<li><a href="https://zetcode.com/terms-testing/test-suite/">Test Suite Tutorial: Definition, Types, and Best Practices | ZetCode</a></li>

</ul>
</details>

**社区讨论**: 最初的提议引发了关于 AI 时代开源商业模式可持续性的讨论。尽管该议题后来被揭示为一个玩笑，但它引发的根本担忧——即 AI 可以将全面的测试用作复制的蓝图——被认为是有效的，并反映了一个真实的行业挑战。维护者最后的评论将焦点从代码保护转向了持续创新和良好产品决策的价值。

**标签**: `#open-source`, `#business-models`, `#testing`, `#ai`, `#intellectual-property`

---

<a id="item-7"></a>
## [开发者一夜之间使用 vibe coding 为 LLM 演讲创建自定义 macOS 演示应用](https://simonwillison.net/2026/Feb/25/present/#atom-everything) ⭐️ 7.0/10

Simon Willison 在 Social Science FOO Camp 的题为'The State of LLMs, February 2026 edition'的非会议演讲前夜，用大约 45 分钟创建了一个名为'Present'的自定义 macOS 演示应用。该应用使用 Swift 和 SwiftUI 构建，仅重 355KB，并通过加载 URL 序列将幻灯片呈现为一系列网页。 这展示了 AI 辅助的'vibe coding'开发实践如何能够快速原型化解决特定工作流程痛点的专用工具，本例中创建了一个比基于浏览器的演示更可靠的替代方案。它突显了开发者如何能够为小众需求快速构建定制解决方案，而不是依赖通用软件，这可能会影响为技术演讲设计演示工具的方式。 该应用解决了 Willison 曾遇到的一个具体问题：在使用多个网页标签作为幻灯片的演示过程中，浏览器崩溃可能导致整个演示文稿丢失。Present.app 在本地存储 URL 并在需要时重新加载它们，在保持基于网络内容的灵活性的同时提供了一个安全网。开发过程是由对所需功能的自然语言描述所促成的。

rss · Simon Willison · Feb 25, 16:46

**背景**: Vibe coding 是一种新兴的软件开发实践，它使用人工智能从自然语言提示生成功能代码，从而加速开发。非会议是一种参与者驱动的会议形式，与会者协作创建议程并主持会议，FOO Camp 是由 O'Reilly Media 主办的年度仅限受邀参加的技术创新者非会议。Simon Willison 是一位以 Datasette 项目和对 LLM 发展的撰文而闻名的开发者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cloud.google.com/discover/what-is-vibe-coding">Vibe Coding Explained: Tools and Guides | Google Cloud</a></li>
<li><a href="https://en.wikipedia.org/wiki/Unconference">Unconference - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Foo_Camp">Foo Camp - Wikipedia</a></li>

</ul>
</details>

**标签**: `#rapid-prototyping`, `#macos-development`, `#presentation-tools`, `#llm-landscape`, `#developer-workflow`

---

<a id="item-8"></a>
## [连接标准联盟发布 Aliro 1.0 规范，统一移动访问控制标准](https://csa-iot.org/newsroom/introducing-aliro-1-0-a-unified-standard-to-transform-the-access-control-ecosystem/) ⭐️ 7.0/10

连接标准联盟（CSA）正式发布了 Aliro 1.0 规范，旨在为使用智能手机和可穿戴设备进行移动访问控制建立一个统一的通信标准。该标准已获得 Apple、Google 和 Samsung 的支持，将深度集成到主流移动钱包中，并支持 NFC、低功耗蓝牙和 UWB 技术。 这很重要，因为它创建了一个由行业支持的统一标准，有望取代分散的专有系统，让用户能更便捷地在办公室、校园、酒店和住宅等场景使用手机开门。由于获得了主要科技公司的支持，Aliro 有潜力成为安全、便捷的移动访问控制的主导协议，从而推动物联网生态系统中更广泛的采用和互操作性。 该规范采用非对称加密技术，以确保用户设备与读卡器之间的安全可信交互，同时保护用户隐私。它旨在通过整合多种传输技术来满足不同的安装需求：NFC 用于“轻触解锁”，低功耗蓝牙用于较长距离通信，而 UWB 与低功耗蓝牙结合则用于实现安全、无感的身份验证。

telegram · zaihuapd · Feb 27, 04:00

**背景**: 连接标准联盟（CSA）是一个开发和推广物联网（IoT）通用开放标准的行业联盟。移动访问控制是指使用智能手机或可穿戴设备作为数字钥匙来开门，以取代物理钥匙或门卡。NFC、低功耗蓝牙和超宽带等技术是短距离无线通信协议，在访问控制场景中，它们在距离、范围和安全性方面各有不同特点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://csa-iot.org/all-solutions/aliro/">Aliro - CSA-IOT</a></li>
<li><a href="https://homekitnews.com/2026/02/26/csa-announces-aliro-1-0-unified-access-control-for-smart-locks/">CSA Announces Aliro 1.0: Unified Access Control For Smart Locks</a></li>
<li><a href="https://en.wikipedia.org/wiki/Ultra-wideband">Ultra -wideband - Wikipedia</a></li>

</ul>
</details>

**标签**: `#IoT Standards`, `#Mobile Access Control`, `#Wireless Protocols`, `#Industry Collaboration`, `#Smartphone Integration`

---

<a id="item-9"></a>
## [逾 200 名 Google 与 OpenAI 员工联署声援 Anthropic 限制军事与监控用途](https://www.axios.com/2026/02/27/google-openai-workers-push-for-military-ai-limits) ⭐️ 7.0/10

超过 200 名来自 Google 和 OpenAI 的员工签署了一封公开信，声援 Anthropic 限制先进 AI 用于国内监控或完全自主武器的政策。公开信披露，美国国防部正与 Google 和 OpenAI 谈判，试图让其接受 Anthropic 已拒绝的用途，并呼吁两家公司的领导层采取一致的立场。 这次集体行动代表了领先 AI 公司内部技术人员对一个关键伦理问题施加的重大内部压力，可能影响公司政策和政府合同。它凸显了行业内关于前沿 AI 模型在军事和监控应用上的可接受性方面日益增长的分歧。 组织者声明该行动独立于任何 AI 公司或政治团体，签名经过核验且可匿名。截至太平洋时间周四下午 5 点 30 分，签署者包括 160 多名 Google 员工和 40 多名 OpenAI 员工。公开信还指出，Google 已于 2025 年 2 月撤销了其内部关于 AI 用于武器和监控的禁令。

telegram · zaihuapd · Feb 27, 09:50

**背景**: Anthropic 是一家 AI 安全和研究公司，以其 Claude 模型而闻名，它作为一家公益公司运营，专注于开发安全的 AI。完全自主武器是指启动后无需人类干预即可选择和攻击目标的系统，这一概念与人类操作的无人机不同。AI 增强的国内监控涉及使用人工智能分析来自摄像头和社交媒体等来源的数据以进行监控，这引发了重大的公民自由关切。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anthropic">Anthropic - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lethal_autonomous_weapon">Lethal autonomous weapon - Wikipedia</a></li>
<li><a href="https://www.brookings.edu/articles/how-ai-can-enable-public-surveillance/">How AI can enable public surveillance - Brookings</a></li>

</ul>
</details>

**标签**: `#AI Ethics`, `#Industry News`, `#Corporate Governance`, `#Military AI`, `#Employee Advocacy`

---