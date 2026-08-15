# Day 7: Claude Model Selection & Reasoning Effort

## Objective

Day 7 was designed to teach how to pick the right Claude model and reasoning effort level based on the task, instead of using one model and one effort setting for everything.

Model selection matters because Haiku, Sonnet, and Opus are built for different kinds of work, and each uses rate limit differently. Using a heavier model than a task needs wastes tokens and slows things down. Using a lighter model than a task needs produces weaker output. The same logic applies to reasoning effort — it controls how much depth Claude applies before answering, independent of which model is picked.

## What I Learned

**Haiku** — the lightest, fastest model. Built for quick answers, simple extraction, and straightforward tasks that don't need deep reasoning.

**Sonnet** — the general-purpose daily driver. Handles writing, coding, analysis, and multi-step workflows. Capable enough that most day-to-day problems don't outgrow it.

**Opus** — a heavier reasoning specialist. Meant for complex, sustained thinking — not routine work. Uses more of the rate limit, so it should be reserved for tasks that genuinely need it.

**Reasoning Effort** — a separate dial from the model itself. It controls how much thinking Claude does before responding.

- **Low** — fastest, lightest, for simple tasks.
- **Standard** — the default balance for most work.
- **High** — for tasks where output quality is worth the extra depth.
- **Max** — reserved for genuinely hard problems; slower and more token-heavy.

## My Profile & Claude Usage

Answers I gave Claude for this exercise:

- **Current situation:** Student — BCA student and Graphic Designer, also doing freelance/project-based graphic design work.
- **Primary activities:** Graphic design, Canva design, Photoshop and Illustrator learning, portfolio building, career preparation, AI tools, prompt engineering, AI projects, web development and coding assistance, content creation, research.
- **Claude usage frequency:** Daily.
- **Types of outputs needed most:** Coding/technical help, content creation & creative work, learning & deep research, career prep & business strategy.

## My Recommended Primary Model

**Sonnet** was recommended as my primary model.

My workflow spans graphic design learning, Canva/Photoshop/Illustrator learning, portfolio development, resume development, LinkedIn content, GitHub documentation, prompt engineering, HTML/CSS/JS support, AI tools and experimentation, the Qelvix project, and career preparation. Graphic Design remains my primary professional direction, with AI and coding as supporting skills.

Sonnet fits this mix because it's a strong generalist across writing, coding, and analysis, and because I use Claude daily — a heavier model would burn through rate limit faster without adding real value to most of these tasks.

## When I Should Use Each Model

### Haiku
For quick, simple, low-stakes tasks: rewriting a caption, formatting cleanup, a fast factual check, a one-line summary. Anything where speed matters more than depth.

### Sonnet
My everyday/default model. Covers design learning, resume and portfolio drafting, LinkedIn content, GitHub documentation, prompt engineering, and HTML/CSS/JS support — the bulk of what I actually do with Claude day to day.

### Opus
Only for genuinely complex work: Qelvix architecture and system planning, deep multi-source research, or a difficult strategic decision I'd want to question and redirect as I go. Not for routine work — using Opus by default would waste rate limit on tasks Sonnet already handles well.

## Reasoning Effort Strategy

### Low
Quick captions, formatting fixes, one-line rewrites, simple checks — tasks from my actual workflow that don't need reasoning depth.

### Standard
My default. Covers design learning, LinkedIn content, GitHub day documentation, HTML/CSS/JS help, and prompt engineering — routine daily work where the default balance is already enough.

### High
For resume and portfolio work, debugging, and detailed documentation — output where quality directly affects a real outcome, so the extra depth is worth it.

### Max
Reserved for genuinely hard problems like Qelvix architecture planning. Rare, because it's slower and uses more of the rate limit, and most tasks don't need that level of depth.

## My Personalized Claude Workflow

| Task | Best Model | Best Effort | Reason |
|---|---|---|---|
| Canva captions / quick social copy | Haiku | Low | Simple, fast, no deep reasoning needed |
| Photoshop / Illustrator learning | Sonnet | Standard | Explanatory, routine daily learning |
| Portfolio / resume work | Sonnet | High | High-stakes output, worth extra depth |
| LinkedIn content | Sonnet | Standard | Routine creative writing |
| GitHub Day documentation | Sonnet | Standard | Structured but repeatable |
| HTML / CSS / JS | Sonnet | Standard | Sonnet handles coding well at moderate cost |
| Prompt engineering | Sonnet | Standard | Conceptual, iterative daily work |
| Qelvix architecture | Opus | High / Max | Complex, sustained system-design reasoning |
| Job-search / market research | Sonnet or Opus | Standard–High | Sonnet for quick pulls, Opus if multi-source and deep |
| Quick formatting / factual checks | Haiku | Low | Instant, minimal rate-limit cost |

## Biggest Mistakes I Should Avoid

- Defaulting to Opus for routine work — wastes rate limit for no quality gain as a daily user.
- Using Haiku for high-stakes writing — resume, cover letters, and portfolio copy need Sonnet at High effort, not the lightest model.
- Using Max effort unnecessarily — it's slower and more token-heavy without guaranteeing a better answer.
- Using higher effort when a simple task doesn't require it — a one-line caption doesn't need Standard or High.
- Choosing a model out of habit instead of matching it to task complexity.

## My Final Default

**One model: Sonnet. One effort level: Standard.**

This combination fits most of my daily workflow — design learning, content creation, coding help, resume work, and challenge documentation — without wasting my daily rate limit.

I move to **High** when the output is resume-grade, portfolio-grade, or otherwise high-stakes. I move to **Opus** when I'm deep in Qelvix-level system thinking or genuinely complex, multi-source research — not for anything Sonnet already handles well.

## Practical Decision Rule

- Quick/simple task → **Haiku + Low**
- Normal daily work → **Sonnet + Standard**
- Important / complex work → **Sonnet + High**
- Deep reasoning / complex architecture / difficult research → **Opus + High or Max**

This is my personalized workflow based on my own profile and activities — not a universal rule for every Claude user.

## Key Takeaways

- The best model is determined by the task, not by defaulting to the most powerful one.
- Model choice and reasoning effort are two separate dials — both need to match the task.
- Sonnet at Standard effort covers most daily work efficiently.
- Reserving Opus and Max for genuinely complex tasks protects rate limit without sacrificing quality where it matters.
- Matching effort to stakes (Low for routine, High for high-stakes) is as important as matching the model itself.

## Evidence

- `claude-usage-strategy.png`

## Day 7 Reflection

Before this exercise I was using whatever model loaded by default, without really thinking about whether the task needed it. Going through the Q&A made it clear that my actual workload — design learning, content, documentation, coding help — is mostly Sonnet-level work, and that I only need Opus for something like Qelvix. The effort setting was the bigger unlock for me; I hadn't been treating it as a separate lever from the model choice at all.

## Submission

Final deliverable for Day 7: the GitHub commit URL for this documentation.
