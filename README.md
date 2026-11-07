# Kiro Study Buddy

# AWS Study Buddy (Fork Otimizado)

> Ferramenta interativa de estudos e simulador de exames para certificações da AWS, com foco atual na **AWS Certified Cloud Practitioner (CLF-C02)**.

## 💡 Créditos e Agradecimentos
Este repositório é um fork otimizado baseado no projeto original desenvolvido por **Filipe Guimarães**, que estruturou a base inicial para o balanceamento de alternativas em simuladores AWS. Nossos sinceros agradecimentos pela excelente contribuição à comunidade!

> A [Kiro](https://kiro.dev) power designed to turn Kiro into a personal study companion for **AWS certification exams**.

![Kiro](https://img.shields.io/badge/Kiro-Power-FF9900?style=flat-square)
![AWS](https://img.shields.io/badge/AWS-Certification-232F3E?style=flat-square&logo=amazon-aws)
![License: MIT](https://img.shields.io/badge/License-MIT-blue?style=flat-square)
![Status: Active](https://img.shields.io/badge/status-active-success?style=flat-square)

Grounded in official AWS documentation via a bundled MCP server. No guessing, no hallucinations, no AWS credentials required.

---

## Table of Contents

- [Why this power?](#why-this-power)
- [Features](#features)
- [Supported exams](#supported-exams)
- [Recursos oficiais e dicas de estudo para a CLF-C02](#recursos-oficiais-e-dicas-de-estudo-para-a-clf-c02)
- [Recommended models](#recommended-models)
- [Installation](#installation)
  - [Guia em português para a turma](./GUIA-PARA-TURMA.md)
  - [Uso com Google Antigravity no VS Code](./GUIA-PARA-TURMA.md#usar-no-vs-code-com-a-extensao-google-antigravity)
- [Usage](#usage)
- [How it works](#how-it-works)
- [Troubleshooting](#troubleshooting)
- [Disclaimer](#disclaimer)
- [Responsible AI](#responsible-ai)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

---

## Why this power?

AWS certification exams are scenario-based — they test architectural thinking, not memorization. Passive study (videos, flashcards) only takes you so far. You need **active practice** with realistic scenarios, feedback grounded in official sources, and timed simulations that build exam-day muscle.

This power gives you all of that inside Kiro. Install once and you have five complementary study modes that adapt to whichever AWS certification you're preparing for.

It's especially useful for:

- **Anyone preparing for an AWS certification** — from Cloud Practitioner to Specialty exams
- **Teams studying together** — install once, consistent study experience for everyone
- **Active learners** who want structured practice instead of passive video watching

## Features

- 🎯 **Always-on study context** — every Kiro response is tailored for your chosen AWS exam: simple language, exam domain mapping, and citations from official AWS documentation.
- 🧠 **Socratic scenario practice** — Kiro presents realistic customer scenarios and guides you to the answer through questions instead of dumping solutions.
- 🔍 **Service comparator** — structured side-by-side comparisons (use cases, trade-offs, decision flowcharts) for the service pairs that matter most for your exam.
- ⏱️ **Timed exam simulator** — practice under real exam conditions with dynamic time budgets, multiple choice and multiple response questions (including select-three for Professional and Specialty exams), time tracking, scoring, pass/fail projection, and a visual exam transcript with scaled scoring and domain performance breakdown. Optionally save transcripts as markdown files to track progress over time.
- 🔬 **Question breakdown method** — practice a structured four-step approach to deconstructing exam questions: identify keywords, eliminate wrong answers, choose between remaining options, and reflect on the concept tested.
- 📚 **Official sources only** — every answer cites AWS documentation. Bundled MCP server pulls from [docs.aws.amazon.com](https://docs.aws.amazon.com) in real time.

## Supported exams

This power is designed to work with current AWS certification exams. At session start, you tell Kiro which exam you're studying for, and it automatically looks up the exam's structure (domains, weights, question count, time limit, passing score) from official AWS documentation.

Examples:

| Level | Exam Code | Exam Name |
|-------|-----------|-----------|
| Foundational | CLF-C02 | AWS Certified Cloud Practitioner |
| Foundational | AIF-C01 | AWS Certified AI Practitioner |
| Associate | SAA-C03 | AWS Certified Solutions Architect - Associate |
| Associate | DVA-C02 | AWS Certified Developer - Associate |
| Associate | SOA-C03 | AWS Certified CloudOps Engineer - Associate |
| Associate | DEA-C01 | AWS Certified Data Engineer - Associate |
| Associate | MLA-C01 | AWS Certified Machine Learning Engineer - Associate |
| Professional | SAP-C02 | AWS Certified Solutions Architect - Professional |
| Professional | DOP-C02 | AWS Certified DevOps Engineer - Professional |
| Professional | AIP-C01 | AWS Certified Generative AI Developer - Professional |
| Specialty | ANS-C01 | AWS Certified Advanced Networking - Specialty |
| Specialty | SCS-C03 | AWS Certified Security - Specialty |
| Specialty | MLS-C01 | AWS Certified Machine Learning - Specialty |

> Current AWS certification exam codes are supported. Kiro looks up the exam guide dynamically.

## Recursos oficiais e dicas de estudo para a CLF-C02

Esta seção é voltada a quem está se preparando para a **AWS Certified Cloud Practitioner (CLF-C02)**. O AWS Study Buddy continua oferecendo suporte a outras certificações AWS; para consultar a ementa de outro exame, use o guia oficial correspondente.

### Ementa oficial do exame

De acordo com o [guia oficial da CLF-C02](https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html), o conteúdo é dividido em quatro domínios:

| Domínio | Peso do conteúdo pontuado |
|---|---:|
| Cloud Concepts | 24% |
| Security and Compliance | 30% |
| Cloud Technology and Services | 34% |
| Billing, Pricing, and Support | 12% |

Os pesos e objetivos podem ser atualizados pela AWS. Consulte o [guia oficial do exame](https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html) para verificar as informações vigentes e os tópicos detalhados de cada domínio. A AWS também informa que o guia não é uma lista completa de todo o conteúdo que pode aparecer na prova.

### Materiais recomendados

- **[AWS Cloud Practitioner Essentials](https://aws.amazon.com/pt/training/course-descriptions/cloud-practitioner-essentials/):** curso digital gratuito da AWS sobre fundamentos de nuvem, serviços, segurança, arquitetura, preços e suporte.
- **[Página oficial da certificação](https://aws.amazon.com/pt/certification/certified-cloud-practitioner/):** informações sobre o exame e a certificação.
- **[AWS Well-Architected](https://aws.amazon.com/pt/architecture/well-architected/):** leitura complementar para conhecer princípios de arquitetura na AWS; não é necessário tratar o material completo como requisito para a CLF-C02.
- **[FAQs da AWS](https://aws.amazon.com/pt/faqs/):** consulte as perguntas frequentes do serviço relacionado ao assunto que estiver estudando.

### Dicas de preparação

- Estude os domínios conforme os pesos do guia oficial, sem deixar de revisar os quatro.
- Ao fazer simulados, procure entender por que a resposta escolhida é a melhor e por que as outras alternativas não atendem tão bem ao cenário.
- Use os simulados como prática: as questões geradas pelo Study Buddy **não são questões oficiais** e não garantem aprovação.
- A prática com serviços AWS é opcional para esta certificação. Se decidir experimentar serviços na sua conta, confira preços, limites e condições atuais para evitar cobranças inesperadas.
- Organize os estudos em sessões regulares e use o guia oficial como referência principal. Cursos, FAQs, artigos e simulados são materiais complementares.

## Recommended models

This power was developed and tested with **Claude Opus** and **Claude Sonnet**. The study modes vary in complexity — modes that evaluate your answers require stronger attention to detail than modes that explain concepts.

| Mode | Recommended Model | Why |
|------|-------------------|-----|
| Exam Simulator | Claude Opus | Evaluates multi-option answers, cross-references 4–6 options against your justification, maintains scoring accuracy |
| Scenario Practice | Claude Opus | Evaluates your reasoning at each step, grades responses, guides without revealing the answer |
| Service Comparator | Claude Sonnet | Structured output from documentation lookups, no answer evaluation |
| Question Breakdown | Claude Opus | Evaluates student keyword analysis, elimination reasoning, and answer selection at each step |
| Study Companion | Claude Sonnet | Concept explanations, citations, follow-up questions |

The key distinction: when the model acts as a **judge** (evaluating your answers), use Claude Opus. When it acts as an **explainer** (presenting information), Claude Sonnet handles it well and responds faster.

> [!NOTE]
> Claude Sonnet can be used for the Exam Simulator and Scenario Practice modes, but with caution — it may occasionally misattribute details between answer options during evaluation feedback. Always verify the feedback against the original question text.

### How to select the model in Kiro

1. Open Kiro
2. Start a new chat or open an existing one
3. Choose the **model selector** at the bottom of the chat input area
4. Choose **Claude Opus** or **Claude Sonnet** from the list
5. The selected model applies to that chat session

> [!IMPORTANT]
> Only Claude Opus and Claude Sonnet have been tested with this power. Other models may work but are not validated — use them at your own risk.

## Installation

### Prerequisites

| Requirement | Purpose | Install |
|-------------|---------|---------|
| [Kiro IDE](https://kiro.dev) | Runs the power | [Download](https://kiro.dev) |
| [Git](https://git-scm.com/) *(optional)* | Clone the repository | [Install guide](https://git-scm.com/downloads) |
| [`uv`](https://docs.astral.sh/uv/) | Runs the bundled MCP server | [Install guide](https://docs.astral.sh/uv/getting-started/installation/) |

No AWS account or credentials needed — the bundled MCP server only reads public AWS documentation.

The AWS Documentation MCP server does not require an API key. Anyone who installs or forks this repository can use the power with their own Kiro setup, provided they have access to a model in Kiro, `uv` installed, and an internet connection. A fork copies the project files and configuration; it does not provide access to the original author's Kiro account, model usage, or quotas.

Kiro offers a **free plan** for individual use, subject to its current usage credits, model availability, and terms. Each student needs their own Kiro account; this repository and its AWS documentation MCP server are free to use and do not require an AWS API key. Check the [current Kiro plans and limits](https://kiro.dev/pricing/) before you start. Usage beyond the free plan's included allowance may require a paid plan.

### Steps

Choose one of the three installation methods:

**Option A — Install directly from GitHub (recommended):**

1. Open Kiro
2. Open the **Powers panel** from the sidebar
3. Choose **Add power from GitHub URL**
4. Enter: `https://github.com/Jesuinoaraujo/aws-study-buddy`

**Option B — Clone with Git:**

```bash
git clone https://github.com/Jesuinoaraujo/aws-study-buddy.git
```

Then:
1. Open Kiro
2. Open the **Powers panel** from the sidebar
3. Choose **Add power from Local Path**
4. Select the cloned folder (the one with `POWER.md` at its root)

**Option C — Download ZIP (no Git required):**

1. Open [your AWS Study Buddy repository on GitHub](https://github.com/Jesuinoaraujo/aws-study-buddy)
2. Select the **Code** button
3. Choose **Download ZIP**
4. Extract the downloaded archive to a folder on your machine
5. Open Kiro
6. Open the **Powers panel** from the sidebar
7. Choose **Add power from Local Path**
8. Select the extracted folder (the one with `POWER.md` at its root)

### Verify the installation

Open any workspace folder in Kiro, then ask:

```
I'm studying for an AWS certification. What is Amazon S3?
```

Kiro will ask which exam you're preparing for, look up the exam structure, and then explain S3 in simple terms mapped to your exam's domains.

> [!NOTE]
> Kiro requires a workspace folder to be open for powers to activate. If you don't have a project to use, create an empty folder (e.g., `~/aws-study`) and open it in Kiro.

## Usage

### Starting a session

When you first interact with the power, Kiro will ask which AWS certification exam you're studying for. Provide the exam name and code:

```
I'm studying for the SAA-C03 exam.
```

Kiro will look up the exam's official metadata (domains, weights, question count, time limit, passing score) and confirm it with you. From that point on, all study content is tailored to your exam.

### Learn a concept

```
What is the AWS Well-Architected Framework?
Explain the shared responsibility model.
What's the difference between a public and private subnet?
```

Every response includes a plain-language explanation, relevant exam domain mapping, official documentation links, and a follow-up question to reinforce learning.

### Compare services

```
Compare Amazon RDS Multi-AZ vs Read Replicas
When would I use Amazon SQS vs Amazon SNS vs Amazon EventBridge?
Reserved Instances vs Savings Plans vs Spot Instances
```

You get a comparison table, exam-angle notes (keywords that signal which to pick), a real-world analogy, and a quick decision flowchart — all mapped to your exam's domains.

### Practice scenarios (Socratic method)

```
Give me a scenario for my exam's first domain
I want to practice at advanced difficulty
Give me a scenario that combines two domains
```

Kiro presents a realistic customer scenario, asks guiding questions, corrects your reasoning with official references, and summarizes the architectural principles at the end.

### Run a timed exam simulation

```
Give me a set of 5 exam-like questions
Give me 10 questions focused on my weakest domain
```

**Exam simulator flow:**

1. Kiro confirms the time budget (dynamically calculated from your exam's time limit and question count) and session rules
2. Enter `Start` to begin
3. Question appears — the timer starts
4. Enter `Ready` when you've decided — the timer stops
5. Enter your answer and justification (not timed)
6. Kiro evaluates: ✅ correct / ⚠️ partially correct / ❌ incorrect, explains why, shows your time
7. Enter `Next` when you've finished reading the analysis — the next timer starts only then
8. After all questions: full summary with score, time breakdown, domain-level performance, and pass/fail projection using your exam's actual passing score
9. Exam transcript: scaled score (100–1000), pass/fail status with a congratulatory or encouragement message, and a domain performance table showing "Needs Improvement" or "Meets Competencies" per domain
10. Optional: save the transcript as a markdown file to `ExamResults/<EXAM_CODE>/` for progress tracking

Questions mix the formats used on real AWS exams:

- **Multiple choice** (majority): pick 1 of 4 options
- **Multiple response (select two)**: pick 2 of 5 options
- **Multiple response (select three)**: pick 3 of 6 options — Professional and Specialty exams only

You must select all correct answers to receive credit for multiple response questions.

### Break down a question

```
#question-breakdown
Generate a question for me to break down
I want to paste my own question
```

Kiro walks you through a four-step method for approaching exam questions:

1. **Identify keywords** — extract the main keywords, objective, and constraints from the scenario
2. **Eliminate wrong answers** — cross off options that are clearly wrong given the constraints
3. **Choose the correct answer** — differentiate between remaining plausible options
4. **Reflect** — summarize the concept tested, distractor pattern, and your confidence level

At each step, you try first, then Kiro compares your analysis with its own — building the metacognitive skill of *how* to think through questions, not just *what* to answer.

## How it works

The power bundles three components:

```
power-aws-study-buddy/
├── POWER.md              # Power metadata, activation keywords, steering routing
├── mcp.json              # AWS Documentation MCP server config
└── steering/
    ├── global-instructions.md      # Cross-cutting rules (no guessing, official sources)
    ├── study.md                    # Always-on study context + exam selection flow
    ├── scenario-practice.md        # Socratic practice mode instructions
    ├── service-comparator.md       # Comparison mode instructions
    ├── question-breakdown.md       # Question breakdown method instructions
    └── exam-simulator.md           # Exam simulator flow and scoring rules
```

- **`POWER.md`** defines when Kiro activates the power (based on keywords like `aws`, `certification`, `exam`, `study`) and which steering file to load for each intent.
- **`mcp.json`** configures the [`awslabs.aws-documentation-mcp-server`](https://awslabs.github.io/mcp/servers/aws-documentation-mcp-server), which gives Kiro real-time access to official AWS documentation.
- **`steering/`** contains the instructions Kiro follows in each study mode. At session start, `study.md` establishes the exam context (which certification you're studying for), and all modes use that context to tailor their content.

## Troubleshooting

### The power doesn't seem to activate

- **Open a workspace.** Kiro requires a folder open to activate powers. Any folder works — even an empty one.
- **Restart Kiro.** Newly installed powers sometimes require a restart.
- **Check the Powers panel.** Confirm the power is listed as installed and enabled.

### `uv` / `uvx` command not found

Install `uv` following the [official guide](https://docs.astral.sh/uv/getting-started/installation/):

**macOS (Homebrew):**
```bash
brew install uv
```

**macOS / Linux (standalone installer):**
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**Windows (PowerShell):**
```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

After installing, restart Kiro so it picks up the new PATH.

### MCP server fails to connect

1. Verify `uv` is installed: `uv --version`
2. Test the MCP server manually: `uvx awslabs.aws-documentation-mcp-server@latest --help`
3. Open Kiro's command palette and search for "MCP" to see server status
4. If behind a corporate proxy, check the [AWS Documentation MCP Server env variables](https://awslabs.github.io/mcp/servers/aws-documentation-mcp-server) (notably `MCP_USER_AGENT`)

### Responses aren't tailored to my exam

- Confirm a workspace folder is open
- Check the Powers panel — the power should be **enabled** (not only installed)
- Try mentioning your exam code explicitly (e.g., "I'm studying for SAA-C03") to trigger the exam selection flow

### Kiro seems to have forgotten which exam I'm studying for

This can happen if the conversation context is very long. Tell Kiro your exam code again and it will re-establish the context.

## Disclaimer

This tool is an independent study aid. It is **not** an official AWS Certification product, and it is not affiliated with, endorsed by, or sponsored by Amazon Web Services or the AWS Certification program. It does not contain questions from official AWS question banks, sample exams, or any proprietary exam content — all practice questions are generated dynamically by the AI model based on public AWS documentation. Passing a practice session in this tool does not guarantee, predict, or imply that you will pass the actual AWS certification exam. Exam content, scoring, and pass/fail criteria are determined solely by AWS. Always refer to the [official AWS Certification](https://aws.amazon.com/certification/) website for authoritative exam information.

## Responsible AI

This power uses generative AI to deliver study content. While it is grounded in official AWS documentation via the bundled MCP server, please keep the following in mind:

- **AI-generated content may be inaccurate.** Foundation models may produce inaccurate information. Always verify critical details against [official AWS documentation](https://docs.aws.amazon.com).
- **This tool supplements, it does not replace.** Use it alongside official exam prep resources (AWS Skill Builder, exam guides, whitepapers), not as your sole study source.
- **Exam simulator scores are approximations.** Scaled scores and pass/fail projections are estimates based on your practice session. They do not predict actual exam results.
- **No professional advice.** This power provides study assistance for AWS certifications. It does not constitute professional, legal, or career advice.
- **Human judgment is final.** Verify information against official AWS documentation when needed. This tool supplements your study process.

## Contributing

Issues and pull requests are welcome. If you find questions that feel inaccurate, prompts that don't behave as expected, or want to suggest new study modes, please [open an issue](../../issues).

When contributing:

- Keep all content grounded in official AWS sources (exam guides, AWS documentation)
- Don't invent service features or fabricate exam content
- Match the existing steering file style and tone
- Verify that changes work across AWS certifications, not only a specific one

## License

Distributed under the MIT License. See [`LICENSE`](LICENSE) for details.

## Acknowledgments

- [AWS Certification](https://aws.amazon.com/certification/) — exam content and official study resources
- [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/) — architectural foundation for many AWS exams
- [Kiro](https://kiro.dev) — the agentic IDE that hosts this power
- [awslabs/mcp](https://github.com/awslabs/mcp) — the AWS Documentation MCP server this power bundles
