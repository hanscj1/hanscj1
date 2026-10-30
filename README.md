# YAKKL® and the Rhumb Workflow Protocol™

Hi,

I'm currently working on a number of interesting products, but here is one:

## YAKKL®

**YAKKL®** is the reference implementation of `@rhumbprotocol`.

YAKKL is a complete AI orchestration, workflow, planning, and retention system that adheres to the open-source **Rhumb Workflow Protocol** at `@rhumbprotocol/specs`.

It performs automatic audits to enforce correct builds and verifies whether AI drift has occurred. AI drift is a major problem. When YAKKL detects it, YAKKL reports it and fixes it to get your creative vision back on track.

In addition, YAKKL retains a full history of everything sent, received, and built. It also tags, indexes, and supports full-text search so that you can recall anything, including system prompts and personas you may have used.

YAKKL was created to assist me in building a new generation of crypto products after I saw what appeared to be major shortfalls in security, UX, and more. I did not set out to build YAKKL as a product. However, as I spoke to other leaders, they asked questions like these—not specifically about YAKKL, but about methodologies, AI, and delivery:

1. How many resources or teams were being used, and were they hand-coding or using AI?
2. What timelines were required to build, test, document, and produce production-ready code based on complex architectures?
3. Did AI or AI products help speed up deliverables without sacrificing quality?
4. What about maintenance? How did it work with AI?

These are most likely the same, or similar, questions that many leaders, architects, principals, and others are asking. I was asking them too.

I told the people I was speaking with the truth:

1. On a specific project, especially larger projects, I would use 6 to 9 resources: PM, architect, senior developers, junior developer, QA, documentation, and more.
2. A greenfield project, starting from scratch, could take 6 to 12 months. It could take even longer when attempting to modernize legacy monolithic codebases.
3. You usually need to include a fudge-factor multiplier of 1.25 to 1.5 depending on team members' skill sets, quality of past work, and budget.
4. With AI vendor CLIs, individuals and teams can do a good bit, but AI still cannot perform miracles—not yet. AI still requires the user to be very knowledgeable about how the process works, what different models do, what tokens are, how tokens are computed, and why so many of them are showing up on the bill. These are only a few of the things you really need to know.

A big issue for leaders and teams is this question:

> Which AI vendor CLI or app should I use?

They should be asking:

> Which models work best for the given task without bankrupting the company, or bankrupting a startup before it even starts up?

So, chicken or egg—which comes first?

Another common comment or question I heard was something like this:

> What if I use Haiku or another mini-style model since they are the cheapest?

I get the point, but the answer was not what they were hoping for.

Is that the best model for your tasks? Of course, they could not answer that. They also did not want to pay a few large consulting firms $500+ per hour, and I bet those firms would not either, based on the ones I have hired in the past and the ones I worked for.

Those firms would bring in the $1,500+ per hour resources, where they have written a few utilities that read PDFs and code samples to help determine the correct fit. Even then, they are really making educated guesses.

By this time, you are almost ready to surrender and wave the white flag because we all have other things to work on. I know I was.

I spent three years in the AI, crypto, and security sectors running a multitude of scenarios, working with different AI vendors and their models, not realizing I was using high-cost models with agents running in the background, forgetting about them, and making a hundred more mistakes that cost a lot of money.

If you are a solo developer or founder wanting to build the next best thing, it takes a lot of time and money.

## How YAKKL Started

YAKKL almost formed itself by applying the above lessons to help build out other YAKKL products and projects.

It started with MPs—**Master Plans**—where the real work gets created. YAKKL uses established templates forged from the fires of pain and suffering caused by lost time and money.

Defining activity as accomplishment should be the AI tagline—kidding, sort of.

The MPs helped me find well-camouflaged things I did not expect at the beginning: drift.

Drift is very difficult to find, and a lot of times you do not know it happened until the end.

I put in rules, then more rules, then even more rules, until I had over 100 rules in vendor files like:

- `CLAUDE.md`
- `AGENTS.md`
- `CODEX.md`
- `GEMINI.md`

I put them there because if one was not good enough, then two had to get it done.

Nope.

I even had one high-end AI model tell me that repeating things can help. I believed it and followed that wise advice.

The vendors always have disclaimers saying that AI makes mistakes. It does.

I kept having handoff prompts and other templates either not done at all or filled in with something I did not recognize and could not trace back to any known source.

After digging for well over a week, I found where the drift began to happen and why.

Keep in mind, at this time I was using vendor CLIs, creating `SKILLS.md` files, plugins, extensions, and so on. I had been documenting everything along the way and how to fix it because I had the bright idea that a skill, or something similar, could keep an eye on it and prevent bad things from happening.

It could not.

Do not misunderstand me. These tools are all great, and they have helped make things much easier than the cut, paste, and pray methodology of using website chat tools. Those are good for other reasons, but not for this kind of serious workflow.

By the way, if you see a clickbait title, thumbnail, or whatever that says something like:

> This is the only prompt you will ever need...

I would question it. I am being very nice here.

There is **no such thing** for serious work.

## Taking Control of the Output

The only way I could begin to control output was to take charge of it as much as possible.

For example, I initially created a TypeScript interface that I used to control things and replace some of the rules, because AI models will sometimes decide to read your rules once and then refuse to follow them at other times.

Things had to be consistent.

I ended up pausing other work and creating a CLI in Rust, my favorite language, that I would call from a command at the time. Now, those calls happen through skills in the AI CLIs.

It sort of worked, so I added more controls. Then it went back to similar behavior.

I realized I needed a way to verify almost every build, so I broke the MPs down into smaller units of work called **phases**, and then into even smaller units of work called **sub-phases**. The AI models then began breaking those down into their smallest units, called **tasks**.

That worked a lot better—until it did not.

So I started a rinse-and-repeat cycle, but added more controls. I found the sweet spot with good controls, governance, credentials, rules, and a lot more to keep projects and products on task and on course.

## YAKKL Was Born

YAKKL was born, and I used it to tackle complex crypto work, analysis, and more.

I found that I needed a longer, more detailed process flow that created real software architecture artifacts. Plans from ideas or specs needed to be broken down into the smallest units of work. Models needed to be selected based on the actual needs of each unit of work, without me having to say:

> Use this model now.  
> Now use that one.

This was a big thing for some of the people I had been speaking with.

This led to the **Architectural Path**, where an **Idea** goes through a few **IP Cycles**—Interactive Planning Cycles. During those cycles, ideas, requirements, or other inputs are fleshed out further, including allowing other models to provide their suggestions. I can then pick the one that more closely fits the goal.

You can tune it as long as you want. There are no restrictions.

The Idea is then promoted to an **AVD**—Architectural Vision Document—where the big picture of the idea is captured, along with how it fits existing completed plans and plans in the queue. This can also include an IP Cycle if desired, but that is optional.

The interesting part of AVDs is that they get decomposed into any number of **ACSs**—Architectural Component Documents.

For example, one AVD could be decomposed into 1, 10, or however many ACSs it takes.

ACSs are interesting because they compare, analyze, and determine which model or models are best suited to break work into components. These are smaller units of highly related work, including how they interact with or depend on other MPs or phases, and how they may be part of a dependency chain for others.

These are not necessarily coding components, though code may be one deliverable.

A single ACS could be decomposed into small, medium, or large MPs, depending on complexity and structure. One or more MPs are then created and placed in the `/planning` folder awaiting review and a decision on `/processing`.

## Master Plans and Audits

MPs are where code is generated. Architectural diagrams are created along the Architectural Path described earlier. Tests are created, sometimes in the high hundreds depending on complexity and the level of coverage desired. Documentation is created. Quality audits usually happen every third sub-phase or phase.

YAKKL then prints an audit report showing what was found and applies a score to it.

You can create another quick MP, handled internally since YAKKL already has the data, to fix the issues. Then the primary thread that found the issues runs again with the fixes applied. Once verified, it moves on to the next phase and continues this cycle until the end.

At the end, YAKKL runs a detailed final audit and verifies that the plan created the correct assets, artifacts, tests, documents, and other deliverables.

If successful, it creates a final handoff document that becomes the source of truth. That document goes into the evidence folder to represent what YAKKL did compared to the plan, what was touched, and what was completed. YAKKL then releases all locks.

YAKKL uses locking so no other process can run the same thing. If something has already been run, YAKKL reports it so the process can move on to something else.

## Direct Path vs. Architectural Path

To be clear, YAKKL supports a **Direct Path**, where it creates a small MP without involving the user so that the work is still fully documented.

If YAKKL believes the task would be better served by the Architectural Path, based on the custom AI check it performs, it prompts the user and asks which path to take, including pros and cons.

If the user only wants a super-fast and cheap response with little to no system prompt, YAKKL can do that too. This is like running a normal chat without the overhead of the full system prompt.

By the way, AI CLIs and apps produce system prompts that can consume anywhere from 15,000 to 40,000 tokens before your one-sentence prompt is even included.

YAKKL lets you know this because, unlike AI CLIs, YAKKL is not in business to sell more tokens. It is designed to do the opposite by reducing prompts through minification techniques, removing unnecessary previous context memory while keeping the same cache of system prompts, and avoiding the need to clear and recreate a new cache that spends more tokens.

## Rhumb Workflow Protocol™ *(RWP™)*

If you are interested, I broke out a lot of this into the **Rhumb Workflow Protocol™**—**RWP™**—so you can tie your apps, tools, reporting, and more into a true deterministic process and artifact system.

RWP uses the same templates and process because YAKKL is the full implementation and representative approach for RWP™.

RWP is located at the `@rhumbprotocol` organization and at:

<https://rhumbprotocol.dev>
