# Awesome Code Review Research

A curated, evidence-aware map of research on modern code review, pull-request review, and closely related change-based inspection practices.

For practical code review guidance and resources, visit [awesomecodereviews.com](https://www.awesomecodereviews.com/).

Papers are assigned to one primary topic to keep the list readable. Many papers are relevant to several topics; secondary topics are shown as tags.

Missing important research? Open a pull request and include the publication status, venue, study design and scope, and a one-sentence finding.

## How to read this list

### Publication status

- **PR** — Peer-reviewed and published.
- **Accepted** — Accepted by a peer-reviewed venue; the final issue or proceedings entry may still be pending.
- **Preprint** — Public manuscript without confirmed peer-reviewed publication.
- **Grey literature** — Industry analysis, blog post, report, or other non-peer-reviewed work.

### Evidence profile

Citation count is not a measure of validity. This list therefore reports both the **study design/scope** and an approximate **citation-influence band**.

Common evidence profiles:

- **Systematic review** — Synthesizes a defined body of prior research.
- **Large industrial study** — Uses substantial data or deployment evidence from one or more companies.
- **Multi-project archival study** — Analyses repositories, reviews, or pull requests across several projects.
- **Controlled experiment** — Manipulates conditions to support stronger causal claims within the experimental setting.
- **Mixed methods** — Combines quantitative and qualitative evidence.
- **Qualitative study** — Interviews, observations, or qualitative analysis intended to explain mechanisms and experiences.
- **Tool or benchmark evaluation** — Evaluates an automated technique, dataset, or model.

### Citation influence

Citation bands are approximate snapshots checked in July 2026. Counts differ across Google Scholar, OpenAlex, Semantic Scholar, Scopus, and publisher pages, so they should be treated as a rough indicator of influence only. For a public repository, record one consistent source—preferably OpenAlex—and automate annual refreshes.

- **★★★★★** — 500+ citations
- **★★★★** — 200–499 citations
- **★★★** — 50–199 citations
- **★★** — 10–49 citations
- **★** — 1–9 citations
- **NEW** — Too recent for citation count to be meaningful
- **—** — Not checked

For maintainability, use one citation source consistently—preferably OpenAlex—and record the source and retrieval date in generated metadata.

## Topic taxonomy

| Topic | Main questions |
|---|---|
| Field overviews and taxonomies | What has been studied, how is the field structured, and where are the gaps? |
| Practices, process, and organizational context | How do teams perform code review, and how do practices differ across organizations? |
| Outcomes, effectiveness, and value | What does code review detect or improve, and under which conditions? |
| Reviewability, cognition, and change design | How do change size, ordering, tests, explanations, and presentation affect reviewers? |
| Reviewer selection, participation, workload, and latency | Who reviews, how quickly, and what affects participation or delays? |
| Human factors, communication, conflict, and inclusion | How do social dynamics, emotions, identity, and communication affect review? |
| Security-focused code review | Which security defects are detected or missed, and how can detection improve? |
| Static analysis, bots, and traditional automation | Which review tasks can be automated or supported without generative AI? |
| AI- and LLM-assisted code review | How well do LLM-based reviewers work, and how do they change human workflows? |
| Special contexts | How does code review work in research software, education, or other specific environments? |

---

# Recent peer-reviewed research: 2024–2026

These papers are separated because recent work may be highly relevant despite having few citations. “Recent” is based on publication years 2024–2026; online-first and proceedings dates can differ.

## Field overviews and automation assessments

- [A Roadmap for Modern Code Review: Challenges and Opportunities](https://doi.org/10.1145/3800963) — Yang et al., *ACM Transactions on Software Engineering and Methodology*, 2026. **PR · Systematic roadmap · NEW · Tags: taxonomy, AI, future research.** Consolidates research from 2013–2025 into understanding studies and improvement techniques, and identifies context-aware, value-driven, and human-centred directions for AI-era review.

- [Code Review Automation: Strengths and Weaknesses of the State of the Art](https://doi.org/10.1109/TSE.2023.3348172) — Tufano et al., *IEEE Transactions on Software Engineering*, 2024. **PR · Comparative tool evaluation · ★★★ (~100) · Tags: automation, benchmarks, deep learning.** Shows that automation performance varies substantially by task and evaluation setup, and that strong benchmark results do not by themselves establish production readiness.

## AI- and LLM-assisted code review

- [AI-Assisted Assessment of Coding Practices in Modern Code Review](https://doi.org/10.1145/3664646.3665664) — Vijayvergiya et al., *AIware*, 2024. **PR · Large industrial deployment · ★★★ (~65) · Tags: LLM, coding practices, Google.** Reports that an LLM-based reviewer can generate useful coding-practice comments at industrial scale, while requiring careful filtering, feedback loops, and integration into existing review workflows.

- [Deep Learning-Based Code Reviews: A Paradigm Shift or a Double-Edged Sword?](https://doi.org/10.1109/ICSE55347.2025.00060) — Tufano et al., *ICSE*, 2025. **PR · Controlled experiment with 29 experienced developers and more than 50 review hours · ★★ (~17) · Tags: LLM assistance, attention, defect severity.** LLM suggestions shifted reviewers’ attention toward suggested locations and increased detection of low-severity issues, but did not improve detection of high-severity issues, save time, or increase confidence.

- [Automated Code Review in Practice](https://doi.org/10.1109/ICSE-SEIP66354.2025.00043) — Cihan et al., *ICSE Software Engineering in Practice*, 2025. **PR · Multi-project industrial mixed methods · ★★ (~34) · Tags: LLM, adoption, outcomes.** Across practitioner feedback and deployed projects, automated comments were frequently resolved and produced small quality gains, but also introduced irrelevant comments and did not automatically shorten review cycles.

- [Human and Machine: How Software Engineers Perceive and Engage with AI-Assisted Code Reviews Compared to Their Peers](https://doi.org/10.1109/CHASE66643.2025.00016) — Alami and Ernst, *CHASE*, 2025. **PR · Qualitative study, 20 interviews · ★★ (~30) · Tags: trust, cognitive load, emotional load.** Developers reported less emotional-regulation effort with LLM reviewers, but sometimes more cognitive load from verbose feedback; adoption remained constrained by trust and missing context.

- [Rethinking Code Review Workflows with LLM Assistance: An Empirical Study](https://doi.org/10.1109/ESEM64174.2025.00013) — Aðalsteinsson et al., *ESEM Industry Track*, 2025. **PR · Industrial field study and experiment · NEW · Tags: workflow, trust, change complexity.** Developers particularly valued AI-led review for large or unfamiliar changes, but false positives and insufficient repository context limited confidence and adoption.

- [Accountability in Code Review: The Role of Intrinsic Drivers and the Impact of LLMs](https://doi.org/10.1145/3721127) — Alami et al., *ACM Transactions on Software Engineering and Methodology*, 2025. **PR · Qualitative and conceptual study · ★★ (~19) · Tags: accountability, ownership, human–AI collaboration.** Examines how intrinsic motivation and social responsibility support accountability in review and why replacing human interaction with LLM feedback can alter those mechanisms.

- [Benchmarking LLMs for Fine-Grained Code Review with Enriched Context in Practice](https://doi.org/10.1145/3803437.3805235) — Hu et al., *FSE Industry Track*, 2026. **PR · Benchmark of 67,910 context-enriched review instances plus industrial deployment · NEW · Tags: issue context, code context, LLM.** Finds that textual context improves benchmark performance more than code context alone and that current models remain limited; at ByteDance, using the benchmark as a reward signal improved a self-evolving review tool's measured performance by 61.98%.

- [SWR-Bench: Assessing LLM Performance in Real-World Code Review Comment Generation](https://doi.org/10.1145/3808144) — Zeng et al., *Proceedings of the ACM on Software Engineering*, 2026. **PR · Benchmark of 1,000 manually verified pull requests with full repository context · NEW · Tags: benchmark, repository context, LLM.** Shows that current systems remain weak on realistic, context-rich review-comment generation; combining systems improves results but leaves substantial room below human-quality review.

- [RovoDev Code Reviewer: A Large-Scale Online Evaluation of LLM-Based Code Review Automation at Atlassian](https://doi.org/10.1145/3786583.3786851) — Tantithamthavorn et al., *ICSE Software Engineering in Practice*, 2026. **PR · Large industrial online evaluation · ★ (~5) · Tags: LLM, deployment, cycle time.** Reports that 38.7% of generated comments led to code changes, while observed pull-request cycle time fell by 30.8% and human review comments by 35.6% in the evaluated deployment context.

- [AI-Assisted Fixes to Code Review Comments at Scale](https://doi.org/10.1145/3803437.3805217) — Maddila et al., *FSE Industry Track*, 2026. **PR · 64,000-pair benchmark, randomized safety trial, and production deployment at Meta · NEW · Tags: LLM, automated fixes, deployment.** An initial interface made reviewers more than 5% slower; showing suggestions only to authors removed that regression, and the deployed model reached a 19.7% actionable-to-applied rate—9.2 percentage points above GPT-4o.

- [Engagement in Code Review: Emotional, Behavioral, and Cognitive Dimensions in Peer vs. LLM Interactions](https://doi.org/10.1145/3830405) — Alami and Ernst, *ACM Transactions on Software Engineering and Methodology*, 2026. **PR · Human-centred empirical study · NEW · Tags: engagement, cognition, emotion.** Frames review engagement as cognitive, emotional, and behavioural, showing that peer and LLM interactions create materially different forms of effort and participation.

- [Toward Author-Guided Review: An Agentic Architecture for Reflective Code Review](https://doi.org/10.1145/3786167.3788428) — Davila and Wiese, *AGENT*, 2026. **PR · Prototype architecture · NEW · Tags: agents, reflection, orchestration.** Proposes a multi-agent review architecture intended to improve reasoning and self-correction; evidence remains early-stage until independently evaluated in realistic development settings.

## Human factors and review content

- [Understanding and Effectively Mitigating Code Review Anxiety](https://doi.org/10.1007/s10664-024-10550-9) — Lee et al., *Empirical Software Engineering*, 2024. **PR · Observational model plus randomized waitlist-controlled intervention · ★★ (~13) · Tags: anxiety, avoidance, intervention.** Finds that anxiety is strongly associated with avoidance behaviours such as procrastination and rubber-stamping, and provides initial experimental evidence that a brief cognitive-behavioural workshop can reduce code-review anxiety.

- [Explaining Explanations: An Empirical Study of Explanations in Code Reviews](https://doi.org/10.1145/3708518) — Widyasari et al., *ACM Transactions on Software Engineering and Methodology*, 2025. **PR · Empirical repository study · ★★ (~21) · Tags: rationale, comments, comprehension.** Shows that explanations are an important but unevenly supplied part of review feedback, motivating tools and practices that help reviewers communicate reasons rather than only requested changes.

- [A Qualitative Study on Refactorings Induced by Code Review](https://doi.org/10.1007/s10664-024-10560-7) — Coelho et al., *Empirical Software Engineering*, 2025. **PR · Qualitative repository study · ★★ (~10) · Tags: refactoring, maintainability, review comments.** Characterizes why reviewers request refactorings and how review-triggered refactoring contributes to maintainability beyond direct defect correction.

- [The Interaction of Complexity and Provenance in Code Review Decisions: Evidence from a Controlled Experiment](https://doi.org/10.1145/3808165) — Singh et al., *FSE*, 2026. **PR · Between-subjects experiment with 385 participants · NEW · Tags: complexity, AI provenance, automation bias.** Higher code complexity increased acceptance of incorrect revisions; provenance alone had no main effect, but under high complexity reviewers were more likely to accept incorrect revisions labelled as AI-authored.

- [Assessing Harmful Comments and Specificity in Code Review Feedback at Scale Using Large Language Models](https://doi.org/10.1145/3803437.3805264) — You et al., *FSE Industry Track*, 2026. **PR · More than 204,000 feedback threads from 30 OSS repositories plus data from 45 organizations · NEW · Tags: feedback quality, harmful comments, specificity, LLM.** LLM classifiers reached F1 up to 0.83 for sentiment and 0.67 for specificity; harmful comments were rare, while specificity analysis proved more immediately useful in industrial deployment.

## Reviewer selection and risk-aware workflows

- [Mitigating the Risk of Defects and Improving Knowledge Distribution with Code Reviewer Recommenders](https://doi.org/10.1145/3797070) — Sefidi Esfahani and Rigby, *FSE*, 2026. **PR · Repository analysis and simulation · NEW · Tags: reviewer recommendation, defect risk, knowledge distribution.** Introduces a team-level changeset-safety measure and simulates adding an expert to risky pull requests; the strategy improves modeled defect-finding effectiveness while balancing workload and knowledge distribution, but the outcome is simulated rather than a live causal deployment.

- [Code Reviewer Recommendation for High Risk Diffs at Scale: Workflow, Recommender, and Live Experiments](https://doi.org/10.1145/3803437.3805220) — Paraspatki et al., *FSE Industry Track*, 2026. **PR · Two randomized industrial trials covering more than 20,000 high-risk diffs · NEW · Tags: risk-aware review, reviewer recommendation, A/B test.** A dedicated high-risk workflow increased review depth and reduced final risk classifications by 9.56% with a 0.45% review-time increase; a tailored recommender produced 9.94% more comments and 7.77% more acceptances without significant guardrail regressions.

## Security

- [An Empirical Study of Static Analysis Tools for Secure Code Review](https://doi.org/10.1145/3650212.3680313) — Charoenwet et al., *ISSTA*, 2024. **PR · 319 vulnerabilities and 815 vulnerability-contributing commits across 92 C/C++ projects · ★★★ (~88) · Tags: static analysis, secure review, prioritization.** Finds that tested static-analysis tools can surface useful warnings for some vulnerable changes, but at least 76% of warnings were irrelevant and 22% of vulnerable changes were missed; prioritization improved precision and recall only modestly.

- [Toward Effective Secure Code Reviews: An Empirical Study of Security-Related Coding Weaknesses](https://doi.org/10.1007/s10664-024-10496-y) — Charoenwet et al., *Empirical Software Engineering*, 2024. **PR · Case study of OpenSSL and PHP using 135,560 review comments · ★★ (~25) · Tags: security, coding weaknesses, remediation.** Reviewers raised concerns covering 35 of 40 CWE-699 categories, but only about 37% were fixed in the same review and some changes were merged despite unresolved security concerns.

- [SeRe: A Security-Related Code Review Dataset Aligned with Real-World Review Activities](https://doi.org/10.1145/3744916.3764557) — Zhao et al., *ICSE*, 2026. **Accepted at ICSE · Dataset of 6,732 security-related reviews selected from 373,824 review instances · NEW · Tags: security, dataset, multilingual repositories.** Provides a curated benchmark for security-specific review classification and generation, while its value for production effectiveness still requires downstream validation.

---

# Emerging, not-yet-peer-reviewed work from 2024–2026

These manuscripts are current and potentially useful, but should not be presented as established evidence until peer review, replication, and stable publication metadata are available.

- [A Survey of Code Review Benchmarks and Evaluation Practices in Pre-LLM and LLM Era](https://arxiv.org/abs/2602.13377) — 2026. **Preprint · Systematic survey of 99 papers · NEW · Tags: benchmarks, evaluation, LLM.** Compares 58 pre-LLM and 41 LLM-era studies across five domains and 18 tasks and highlights fragmentation in datasets, metrics, and evaluation protocols.

- [Evaluating Large Language Models for Code Review](https://arxiv.org/abs/2505.20206) — 2025. **Preprint · Comparative model evaluation · NEW · Tags: correctness classification, repair, context.** Reports best-case scores of 68.50% for issue classification and 67.83% for correction, with performance dropping when issue descriptions are absent; the results support human-in-the-loop use rather than autonomous acceptance.

---

# Established peer-reviewed research

## 1. Field overviews and taxonomies

- [A Systematic Literature Review and Taxonomy of Modern Code Review](https://doi.org/10.1016/j.jss.2021.110951) — Davila and Nunes, *Journal of Systems and Software*, 2021. **PR · Systematic review of 139 papers · ★★★ (~70–125) · Tags: taxonomy, research methods.** Organizes the field into foundational studies, proposals, and evaluations and provides a strong starting point for discovering earlier work.

- [Modern Code Reviews—Survey of Literature and Practice](https://doi.org/10.1145/3585004) — Badampudi et al., *ACM Transactions on Software Engineering and Methodology*, 2023. **PR · Review of 244 primary studies plus practitioner survey · ★★★ (~80) · Tags: synthesis, research–practice gap.** Identifies five major research themes and shows that practitioners value quality and process outcomes more consistently than human-factor or support-system claims.

- [A Faceted Classification Scheme for Change-Based Industrial Code Review Processes](https://doi.org/10.1109/QRS.2016.19) — Baum et al., *QRS*, 2016. **PR · Classification grounded in industrial processes · ★★★ (~73) · Tags: process design, industry.** Defines dimensions for comparing change-based review processes instead of treating “code review” as one uniform practice.

## 2. Practices, process, and organizational context

- [Expectations, Outcomes, and Challenges of Modern Code Review](https://doi.org/10.1109/ICSE.2013.6606617) — Bacchelli and Bird, *ICSE*, 2013. **PR · Microsoft mixed methods · ★★★★★ (~500+) · Tags: motivations, knowledge transfer, challenges.** Shows that defect finding is the stated primary motivation, while understanding, knowledge transfer, team awareness, and finding alternative solutions are major practical outcomes.

- [Process Aspects and Social Dynamics of Contemporary Code Review](https://doi.org/10.1109/TSE.2016.2576451) — Bosu et al., *IEEE Transactions on Software Engineering*, 2017. **PR · Comparative Microsoft and OSS study · ★★★ · Tags: process, social dynamics, industry–OSS comparison.** Demonstrates that review outcomes and participation are shaped by both process design and social relationships, with meaningful differences between company and open-source settings.

- [Code Reviewing in the Trenches: Understanding Challenges, Best Practices and Tool Needs](https://www.microsoft.com/en-us/research/publication/code-reviewing-in-the-trenches-understanding-challenges-best-practices-and-tool-needs/) — MacLeod et al., *IEEE Software*, 2018. **PR · Industrial interviews and observations · ★★★ · Tags: reviewer needs, tools, practice.** Identifies recurring practical difficulties including understanding changes, finding suitable reviewers, managing context, and communicating effectively.

- [Modern Code Review: A Case Study at Google](https://research.google/pubs/modern-code-review-a-case-study-at-google/) — Sadowski et al., *ICSE Software Engineering in Practice*, 2018. **PR · Large industrial study: interviews, survey, and 9 million reviewed changes · ★★★★★ (~560) · Tags: Google, process, scale.** Documents Google’s lightweight review process, review norms, tooling, and motivations at very large organizational scale.

- [Code Review Is Just Reviewing Code? A Qualitative Study to Understand the Activities Developers Perform During Code Review](https://doi.org/10.1145/3474624.3477063) — Cunha et al., *SBES*, 2021. **PR · Qualitative study · ★★ (~26) · Tags: activities, collaboration, sensemaking.** Shows that review includes coordination, learning, design discussion, and process work in addition to inspecting code.

- [Developers’ Perception of Peer Code Review in Research Software Development](https://doi.org/10.1007/s10664-021-10053-x) — Eisty and Carver, *Empirical Software Engineering*, 2022. **PR · Survey of research-software developers · ★★ (~41) · Tags: research software, adoption, perceived value.** Finds broad perceived value in peer review but also context-specific barriers involving expertise, resources, and the less standardized nature of research-software teams.

- [Using a Balanced Scorecard to Identify Opportunities to Improve Code Review Effectiveness](https://doi.org/10.1007/s10664-021-10038-w) — Hasan et al., *Empirical Software Engineering*, 2021. **PR · Industrial experience report · ★★ · Tags: measurement, process improvement, dashboards.** Describes a multi-dimensional measurement approach for identifying review bottlenecks and selecting improvement initiatives rather than optimizing a single metric.

## 3. Outcomes, effectiveness, and value

- [The Impact of Code Review Coverage and Code Review Participation on Software Quality](https://doi.org/10.1145/2597073.2597076) — McIntosh et al., *MSR*, 2014. **PR · Multi-project archival study · ★★★ · Tags: coverage, participation, defects.** Reports associations between lower review coverage or participation and poorer post-release quality; the observational design supports association, not a simple causal claim.

- [Modern Code Reviews in Open-Source Projects: Which Problems Do They Fix?](https://doi.org/10.1145/2597073.2597082) — Beller et al., *MSR*, 2014. **PR · Manual classification of more than 1,400 changes · ★★★★ (~350) · Tags: defects, maintainability, OSS.** Finds that review addresses a broad mixture of functional defects, evolvability concerns, and other issues rather than only correctness bugs.

- [Characteristics of Useful Code Reviews: An Empirical Study at Microsoft](https://www.microsoft.com/en-us/research/publication/characteristics-of-useful-code-reviews-an-empirical-study-at-microsoft/) — Bosu et al., *MSR*, 2015. **PR · Microsoft mixed methods · ★★★ · Tags: useful comments, change size, reviewer experience.** Identifies factors associated with useful comments and reports that reviews spanning more files tend to contain a lower proportion of useful feedback.

- [Why Does Code Review Work for Open Source Software Communities?](https://doi.org/10.1109/ICSE.2019.00111) — Alami et al., *ICSE*, 2019. **PR · Qualitative study · ★★★ (~59) · Tags: mechanisms, community, trust.** Explains review effectiveness through community mechanisms such as accountability, transparency, shared ownership, and relationship building—not only defect detection.

- [Do Small Code Changes Merge Faster? A Multi-Language Empirical Investigation](https://doi.org/10.1145/3524842.3528448) — Catolino et al., *MSR*, 2022. **PR · Multi-project archival study · ★★ (~16) · Tags: size, latency, pull requests.** Contrary to common advice, finds no consistent relationship between pull-request size or composition and time to merge in the studied projects.

- [Nudge: Accelerating Overdue Pull Requests Toward Completion](https://doi.org/10.1145/3544791) — Kudrjavets et al., *ACM Transactions on Software Engineering and Methodology*, 2023. **PR · Large industrial intervention · ★★ (~49) · Tags: latency, reminders, workflow.** Reports that targeted automated reminders reduced resolution time for overdue pull requests by roughly 60% in the evaluated deployment.

## 4. Reviewability, cognition, and change design

- [When Testing Meets Code Review: Why and How Developers Review Tests](https://doi.org/10.1145/3180155.3180192) — Spadini et al., *ICSE*, 2018. **PR · Mixed methods · ★★★ (~92) · Tags: tests, reviewer attention, practices.** Shows that developers do review tests, but test review receives uneven attention and involves concerns that differ from production-code review.

- [Test-Driven Code Review: An Empirical Study](https://doi.org/10.1109/ICSE.2019.00110) — Spadini et al., *ICSE*, 2019. **PR · Controlled experiment · ★★★ · Tags: review order, tests, defects.** Reviewing tests before production code led participants to find more test-code defects and fewer maintainability issues in production code, while the number of production-code defects found did not materially change.

- [What Makes a Code Change Easier to Review: An Empirical Investigation on Code Change Reviewability](https://doi.org/10.1145/3236024.3236080) — Baum et al., *ESEC/FSE*, 2018. **PR · Multi-method empirical study · ★★★ · Tags: reviewability, change description, complexity.** Identifies technical and presentation characteristics that affect perceived review difficulty, supporting reviewability as a broader construct than change size alone.

* [Primers or Reminders? The Effects of Existing Review Comments on Code Review](https://doi.org/10.1145/3377811.3380385) — Spadini, Çalikli, and Bacchelli, *ICSE*, 2020. **PR · Controlled experiment with 85 developers · ★★ · Tags: cognitive bias, existing comments, defect detection.** Although approximately 70% of participants showed susceptibility to availability bias, existing comments did not generally bias review outcomes; comments about unusual bug types increased detection of another bug of the same type without reducing detection of unrelated bugs.

- [First Come First Served: The Impact of File Position on Code Review](https://doi.org/10.1145/3540250.3549177) — Fregnan et al., *ESEC/FSE*, 2022. **PR · Large repository study plus controlled experiment · ★★ · Tags: ordering, attention, cognition.** Shows a strong position effect: in the experiment, a defect had substantially lower odds of detection when its file appeared last rather than first.

- [An Exploratory Study on Confusion in Code Reviews](https://doi.org/10.1007/s10664-020-09909-5) — Ebert et al., *Empirical Software Engineering*, 2021. **PR · Qualitative and repository study · ★★★ · Tags: confusion, comprehension, communication.** Characterizes signals and causes of reviewer confusion and shows that unresolved misunderstanding can lengthen discussions and impede review progress.

## 5. Reviewer selection, participation, workload, and latency

- [Impact of Developer Reputation on Code Review Outcomes in OSS Projects](https://doi.org/10.1145/2652524.2652544) — Bosu and Carver, *ESEM*, 2014. **PR · Multi-project archival study · ★★★ · Tags: reputation, acceptance, latency.** Finds that contributor reputation is associated with acceptance, feedback speed, completion time, and the number of patch sets required.

- [Impact of Peer Code Review on Peer Impression Formation: A Survey](https://doi.org/10.1109/ESEM.2013.19) — Bosu and Carver, *ESEM*, 2013. **PR · Survey · ★★ · Tags: trust, reputation, social judgment.** Shows that review interactions shape developers’ impressions of one another, linking technical review behaviour to future collaboration and trust.

- [Does Reviewer Recommendation Help Developers?](https://doi.org/10.1109/TSE.2018.2868367) — Thongtanunam et al., *IEEE Transactions on Software Engineering*, 2020. **PR · Tool evaluation and practitioner study · ★★★ (~70) · Tags: reviewer recommendation, adoption, evaluation.** Finds that recommendations were often perceived as relevant but rarely added practical value beyond developers’ existing knowledge, showing that offline accuracy alone is an insufficient evaluation criterion.

- [Code Reviewer Recommendation in Tencent: Practice, Challenge, and Direction](https://doi.org/10.1145/3510457.3513035) — Rong et al., *ICSE Software Engineering in Practice*, 2022. **PR · Large industrial comparison · ★★ (~15) · Tags: reviewer recommendation, Tencent, deployment.** Compares established recommendation approaches in a production environment and identifies practical constraints—such as organizational structure, workload, and maintainability—that offline benchmarks often omit.

- [Recommending Code Reviewers for Proprietary Software Projects: A Large Scale Study](https://doi.org/10.1109/SANER53432.2022.00080) — Rong et al., *SANER*, 2022. **PR · Large industrial study at Tencent · ★★ (~18) · Tags: reviewer recommendation, proprietary software, scale.** Evaluates reviewer-recommendation techniques on proprietary projects and introduces CAMP, showing that production constraints and organizational context materially affect recommendation usefulness.

## 6. Human factors, communication, conflict, and inclusion

- [Interpersonal Conflicts During Code Review: Developers’ Experience and Practices](https://doi.org/10.1145/3512945) — Wurzel Gonçalves et al., *Proceedings of the ACM on Human-Computer Interaction*, 2022. **PR · Interviews with 22 developers · ★★ (~26) · Tags: conflict, coping, communication.** Characterizes conflict causes, consequences, and developer coping strategies, showing that conflicts can damage relationships and participation even when the technical issue is resolved.

- [Predicting Developers’ Negative Feelings About Code Review](https://doi.org/10.1145/3377811.3380414) — Egelman et al., *ICSE*, 2020. **PR · Large industrial mixed methods · ★★★ (~83) · Tags: negative experience, prediction, organizational climate.** Connects review-process and interaction signals with developers’ negative experiences, enabling teams to study socio-technical review health rather than only throughput.

- [The Pushback Effects of Race, Ethnicity, Gender, and Age in Code Review](https://doi.org/10.1145/3474097) — Murphy-Hill et al., *Communications of the ACM*, 2022. **PR · Large industrial observational study · ★★ · Tags: demographics, pushback, inclusion.** Reports that the amount of pushback authors receive varies with demographic characteristics, while emphasizing that these observational differences require organizational investigation rather than assumptions about individual performance.

- [Engineering Impacts of Anonymous Author Code Review](https://doi.org/10.1109/TSE.2021.3056942) — Murphy-Hill et al., *IEEE Transactions on Software Engineering*, 2022. **PR · Industrial field experiment, 5,217 reviews and 300 engineers · ★★ (~18) · Tags: anonymity, bias mitigation, outcomes.** Tests anonymous-author review in practice and provides direct experimental evidence about its engineering and behavioural effects rather than relying only on observational demographic comparisons.

- [Systemic Gender Inequities in Who Reviews Code](https://doi.org/10.1145/3579527) — Egelman et al., *Proceedings of the ACM on Human-Computer Interaction*, 2023. **PR · Large industrial mixed methods · ★★ (~14) · Tags: reviewer workload, gender, recommender systems.** Finds that women performed about 25% fewer reviews on average and traces the difference to reviewer choice, recommender-system amplification, and unequal access to reviewer credentials.

- [Code Reviews in Open Source Projects: How Do Gender Biases Affect Participation and Outcomes?](https://doi.org/10.1007/s10664-023-10324-9) — Sultana et al., *Empirical Software Engineering*, 2023. **PR · 1,010 projects across 14 datasets · ★★ (~32) · Tags: gender, participation, acceptance, latency.** Finds widespread but context-dependent gender differences; reviewer participation was the most consistently unequal outcome, while the direction of acceptance and latency differences varied across communities.

- [Expressions of Sentiments During Code Reviews: Male vs. Female](https://doi.org/10.1109/SANER.2019.8668027) — Paul et al., *SANER*, 2019. **PR · Multi-project archival study · ★★ · Tags: sentiment, gender, communication.** Reports gender-associated differences in positive and negative sentiment expression across six open-source review communities, while not establishing that sentiment differences are caused by gender.

- [Biases and Differences in Code Review Using Medical Imaging and Eye-Tracking: Genders, Humans, and Machines](https://doi.org/10.1145/3368089.3409681) — Huang et al., *ESEC/FSE*, 2020. **PR · Controlled eye-tracking and neuroimaging study · ★★ · Tags: attention, gender, automation bias.** Finds measurable differences in review attention and evaluation behaviour across participant and code-provenance conditions, illustrating that review judgments can be influenced by factors beyond code content.

- [Automated Identification of Toxic Code Reviews Using ToxiCR](https://doi.org/10.1145/3583562) — Sarker et al., *ACM Transactions on Software Engineering and Methodology*, 2023. **PR · Labelled dataset and classifier evaluation · ★★★ (~80) · Tags: toxicity, NLP, tooling.** Introduces a software-engineering-specific toxicity taxonomy, dataset, and classifier that outperforms general-purpose toxicity detectors on code-review text.

- * [Gender Differences and Bias in Open Source: Pull Request Acceptance of Women Versus Men](https://doi.org/10.7717/peerj-cs.111) — Terrell et al., *PeerJ Computer Science*, 2017. **PR · Large multi-project archival study of roughly 3 million pull requests · ★★★★★ · Tags: gender, acceptance, identity visibility.** Women’s pull requests had higher acceptance rates overall, but among external contributors whose gender was identifiable, women’s contributions were accepted less often than men’s; this difference was not observed when gender was not identifiable.

* [Investigating the Effects of Gender Bias on GitHub](https://doi.org/10.1109/ICSE.2019.00079) — Imtiaz et al., *ICSE*, 2019. **PR · Large-scale quantitative GitHub study · ★★★ · Tags: gender, communication, participation.** Finds little direct evidence of the four investigated gender-bias effects in observable GitHub outcomes, but reports that women concentrated their work in fewer repositories and communicated more restrainedly than men.

* [On the Relationship Between the Developer’s Perceptible Race and Ethnicity and the Evaluation of Contributions in OSS](https://doi.org/10.1109/TSE.2021.3073773) — Nadri et al., *IEEE Transactions on Software Engineering*, 2022. **PR · Large multi-project archival study of more than 2 million pull requests · ★★★ · Tags: race, ethnicity, acceptance, affinity bias.** Contributions from developers perceived as White had approximately 6–10% higher odds of acceptance than contributions from developers perceived as non-White; non-White contributors also had better acceptance odds when the integrator was perceived as belonging to the same racial or ethnic group.


## 7. Security-focused code review

- [Identifying the Characteristics of Vulnerable Code Changes: An Empirical Study](https://doi.org/10.1145/2635868.2635880) — Bosu et al., *FSE*, 2014. **PR · Empirical security study · ★★★ · Tags: vulnerable changes, risk factors, targeting.** Characterizes change properties associated with vulnerability introduction to help teams target scarce security-review attention.

- [A Security Perspective on Code Review: The Case of Chromium](https://doi.org/10.1109/SCAM.2016.30) — Bosu et al., *SCAM*, 2016. **PR · Chromium archival study · ★★★ · Tags: security review, vulnerabilities, reviewer expertise.** Examines how security concerns appear in Chromium review and how reviewer participation and change characteristics relate to security outcomes.

- [A Large-Scale Study of Modern Code Review and Security in Open Source Projects](https://doi.org/10.1145/3127005.3127014) — Thompson and Wagner, *PROMISE*, 2017. **PR · 3,126 projects, 143 languages, 489,038 issues, and 382,771 pull requests · ★★★ (~53) · Tags: security, review coverage, OSS.** Finds associations between modern review practices and security-related outcomes at large scale, while the observational design does not establish that review alone caused those outcomes.

- [Why Don’t Developers Detect Improper Input Validation? `'; DROP TABLE Papers;`](https://doi.org/10.1109/ICSE43902.2021.00054) — Braz et al., *ICSE*, 2021. **PR · Controlled online experiment with 146 participants · ★★ (~38) · Tags: input validation, threat framing, warnings.** Finds that making an attack scenario visible and providing security warnings improves detection of improper input validation during review.

- [Why Security Defects Go Unnoticed During Code Reviews? A Case-Control Study of the Chromium OS Project](https://doi.org/10.1109/ICSE43902.2021.00124) — Paul et al., *ICSE*, 2021. **PR · Case-control study: 516 detected and 374 escaped defects · ★★/★★★ (~36–60) · Tags: escaped defects, workload, review history.** Identifies factors associated with detection and escape, including reviewer load, change spread, mutual-review relationships, and prior file history.

- [Software Security During Modern Code Review: The Developer’s Perspective](https://doi.org/10.1145/3540250.3549135) — Braz and Bacchelli, *ESEC/FSE*, 2022. **PR · 10 interviews plus survey of 182 developers · ★★ · Tags: security mindset, expertise, process.** Shows that developers often treat security as implicit or specialist work and identifies gaps in security knowledge, training, process, and tooling that prevent security from becoming a routine review concern.

## 8. Static analysis, bots, and traditional automation

- [Evaluating How Static Analysis Tools Can Reduce Code Review Effort](https://doi.org/10.1109/VLHCC.2017.8103456) — Panichella et al., *VL/HCC*, 2017. **PR · Comparative empirical study · ★★★ (~114) · Tags: static analysis, reviewer effort, overlap.** Finds that an off-the-shelf static analyser detected about 16% of issues raised manually, with additional potential from project-specific rules; this supports complementing rather than replacing human review.

- [Towards Automating Code Review Activities](https://doi.org/10.1109/ICSE43902.2021.00027) — Tufano et al., *ICSE*, 2021. **PR · Neural-model evaluation · ★★★ · Tags: comment generation, code transformation, automation.** Demonstrates the feasibility of learning selected review activities from historical data while exposing substantial limitations in generalisation and complete end-to-end automation.

- [Using Pre-Trained Models to Boost Code Review Automation](https://doi.org/10.1145/3510003.3510621) — Tufano et al., *ICSE*, 2022. **PR · Large model evaluation · ★★★★ (~306) · Tags: pre-trained models, comment generation, code changes.** Shows that pre-training substantially improves automated review-comment and code-change tasks compared with models trained only on task-specific review data.

- [Investigating the Effects of Code Review Bots on Pull Request Activities](https://doi.org/10.1007/s10664-022-10130-9) — Wessel et al., *Empirical Software Engineering*, 2022. **PR · 1,194 projects plus 12 interviews · ★★ (~41) · Tags: bots, communication, pull-request outcomes.** Associates bot adoption with more merged and fewer abandoned pull requests, while also finding reduced human communication and new integration challenges.

- [Can Static Analysis Tools Find More Defects? A Qualitative Study of Design Rule Violations Found by Code Review](https://doi.org/10.1007/s10664-022-10232-4) — Lenarduzzi et al., *Empirical Software Engineering*, 2023. **PR · Qualitative classification of 1,323 review defects · ★★ · Tags: static analysis, design rules, automation potential.** Finds that many review findings map to rules that static analysis could potentially encode, but theoretical detectability should not be interpreted as demonstrated precision and recall in live review.

---

# Historical foundations and adjacent evidence

These works are useful for understanding modern code review but should not be mixed uncritically with contemporary asynchronous, tool-mediated review.

- [An Exploratory Study of the Pull-Based Software Development Model](https://doi.org/10.1145/2568225.2568260) — Gousios et al., *ICSE*, 2014. **PR · Large multi-project archival study · ★★★★★ (~900) · Tags: pull requests, integration, participation.** Establishes foundational evidence about pull-request contribution, evaluation, integration time, and community participation.

- [The Effect of Familiarity Between Author and Reviewers on the Effectiveness of Code Inspection Meetings](https://www.proquest.com/openview/45a40e77be454b467ab4d058336a1a3b/) — 1999. **Dissertation/non-journal source · Historical inspection study · — · Tags: familiarity, synchronous inspection.** Examines how prior familiarity may affect traditional inspection meetings; applicability to modern asynchronous review should be treated cautiously.

---

# Grey literature and quantitative industry analyses

Keep these in a separate section. They may offer useful scale or practitioner hypotheses, but their sampling, analysis, and review procedures usually provide weaker safeguards than peer-reviewed research.

- [Does Size Matter in Pull Requests? Insights from 30K Developers](https://insights.adadot.com/2023/11/23/does-size-matter-in-pull-requests-insights-from-30k-developers/) — Adadot, 2023. **Grey literature · Proprietary quantitative analysis · Tags: size, latency, developer analytics.** Reports associations between pull-request size and process outcomes, but should be interpreted alongside the peer-reviewed multi-language study that found no consistent size–merge-time relationship.

---

# Recommended contribution format

Use this format for each pull request:

```markdown
- [Paper title](canonical DOI or publisher URL) — Author et al., *Venue*, year. **Status · Evidence profile and sample/scope · Citation band · Tags.** One sentence stating the principal finding without implying causality beyond the study design.
```

Required checks:

1. Use the canonical DOI or official publisher page where possible.
2. Verify the publication year, venue, and peer-review status.
3. State the actual design and scope—for example, “single-company archival study,” not merely “empirical study.”
4. Distinguish observed association from demonstrated causal effect.
5. State null findings explicitly.
6. Do not describe benchmark performance as evidence of production effectiveness.
7. Do not describe citation count as evidence quality.
8. Add a citation-source and retrieval-date field if counts are generated automatically.
9. Re-check the “Recent” sections at least annually and move older work into the topic taxonomy.
