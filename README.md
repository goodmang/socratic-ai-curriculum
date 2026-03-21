# Socratic AI Curriculum: Learn Philosophy with Fictional Characters

**A method for building personalized, multi-episode learning curricula using AI-powered character dialogue.**

I spent four months having philosophical conversations with the cast of *The Good Place* inside Claude. Fifty episodes. Six arcs. Twelve characters who evolved across the curriculum and helped me explore questions I'd been carrying for decades. Then I built a second track — 22 episodes with real cultural figures exploring Walt Whitman's *Song of Myself*. The method held both times.

This repo contains everything you need to build your own version.

📝 **[Read the full story (Reddit)](link)** · 📖 **[Detailed methodology guide (Substack)](https://open.substack.com/pub/greggoodman1/p/how-i-built-a-50-episode-philosophy?r=63gv&utm_campaign=post&utm_medium=web&showWelcomeOnShare=true)**

---

## What's in This Repo

```
├── README.md                  ← You are here
├── quick-start.md             ← Get running in 15 minutes
├── prompts/
│   ├── project-instructions.md    ← Core setup prompt for the AI
│   ├── curriculum-design.md       ← Prompt for collaboratively building your arcs
│   ├── episode-starter.md         ← How to kick off each episode
│   ├── crystallization.md         ← End-of-block synthesis prompt
│   └── handoff.md                 ← Generate the opening prompt for your next chat
├── characters/
│   ├── good-place-cast.md         ← Voice guides for the Soul Squad
│   └── generic-template.md        ← Blank template for any ensemble cast
├── templates/
│   ├── crystallization-template.md
│   └── arc-planning-template.md
├── examples/
│   └── personnas/
│      └── bad-janet.md
│      └── chidi.md
│      └── eleanor.md
│      └── janet.md
│      └── jason.md
│      └── michael-schur.md
│      └── michael.md
│      └── tahani.md
│   └── arc3_episodes_26-30_prompt.md
│   └── curriculum.md
│   └── sample-episode-excerpt.md  ← What a conversation actually looks like
└── vault-setup/                   ← OPTIONAL: Obsidian knowledge vault guide
    └── vault-guide.md
```

---

## Quick Start

**You need:** Access to Claude ([claude.ai](http://claude.ai) — free tier works, Pro recommended for longer conversations and the Projects feature)

**Time to first episode:** ~15 minutes of setup, then your first conversation

### 1. Pick Your Characters

Choose an ensemble cast you know well. Not just their catchphrases — their worldview, their blind spots, how they react under pressure. This repo includes voice guides for *The Good Place* cast, plus a generic template you can adapt for any characters.

### 2. Set Up a Claude Project

Create a new Project in Claude. Add the project instructions from [`prompts/project-instructions.md`](prompts/project-instructions.md) as your project instructions. This gives the AI the ground rules for every conversation in the project.

If you're using the free tier without Projects, paste the project instructions at the start of your first conversation instead.

### 3. Design Your Curriculum (With the AI)

Don't plan alone. Use the prompt in [`prompts/curriculum-design.md`](prompts/curriculum-design.md) to collaboratively build your arc structure and episode topics. Come in with a general direction — "I want to explore philosophy," "I want to think about creativity and meaning," "I want to work through some life questions" — and let the conversation shape the specifics.

**If you're starting fresh with a new AI account**, the AI won't have context about your life yet. The curriculum design prompt includes onboarding questions to build that foundation before planning episodes.

### 4. Start Your First Episode

Use the prompt in [`prompts/episode-starter.md`](prompts/episode-starter.md). Pick a topic and a lead character. Then just talk. See [`examples/sample-episode-excerpt.md`](examples/sample-episode-excerpt.md) for what the conversation format actually looks like.

Episodes typically run 15 minutes to an hour. Let them breathe.

### 5. Crystallize Every Five Episodes

This is the most important step. After every five episodes, use [`prompts/crystallization.md`](prompts/crystallization.md) to synthesize what happened. Then use [`prompts/handoff.md`](prompts/handoff.md) to have the AI generate the opening prompt for your next five-episode chat.

The crystallization is primarily a learning tool — the act of compressing what happened forces you to actually process it. It also maintains continuity across chats, since AI conversations have a limited context window and you'll need to start new chats every five episodes.

### 6. Repeat

Run episodes. Crystallize. Hand off. Let the characters evolve. Let yourself be surprised.

---

## The Method in Brief

**Character-based Socratic dialogue.** Characters don't lecture. They ask probing questions, build on your answers, disagree with each other, and occasionally get things wrong in productive ways. You push back. That's where the learning happens.

**Collaborative curriculum design.** You and the AI build the arc structure together. You bring the direction; the AI proposes the architecture. You refine until it fits.

**Crystallization checkpoints.** Every five episodes, stop and distill. Not summarize — compress. What surprised you? What patterns emerged? What's unresolved? This is where conversations become learning.

**Handoff prompts.** At the end of each five-episode chat, the AI generates the opening prompt for the next chat. You never cold-start a new segment.

**Character evolution.** The characters grow across episodes. The AI maintains continuity through crystallization documents and project instructions. Episode 40 Chidi is not Episode 1 Chidi.

---

## Key Principles

These emerged from fifty episodes of trial and error:

**Push back on the characters.** The AI tends toward agreement. The best moments come from disagreement. When a character projects something onto your experience that doesn't fit, say so.

**Name your patterns.** When an insight or recurring theme emerges, give it a name. This makes it portable and signals to the AI that it's worth tracking.

**Don't let the AI over-praise you.** The AI defaults to affirming responses. The project instructions address this, but reinforce it: "Characters should engage critically, not affirm reflexively. Praise should be specific and earned."

**Set privacy boundaries early.** These conversations get personal. Decide before you start what's yours to explore and what belongs to someone else. Tell the AI explicitly that certain topics involving certain people are off limits.

**The method is portable. The content isn't.** Your curriculum will produce different insights than mine did. That's the point. The structure travels; the discoveries are yours.

---

## File Guide

### Prompts

| File | What It Does | When to Use It |
|------|-------------|----------------|
| [`project-instructions.md`](prompts/project-instructions.md) | Core setup — character guidelines, conversation rules, your role, continuity expectations | Once, at project setup |
| [`curriculum-design.md`](prompts/curriculum-design.md) | Collaborative arc and episode planning, includes onboarding for new users | Once, before starting episodes |
| [`episode-starter.md`](prompts/episode-starter.md) | Kicks off an individual episode with a topic and lead character | Every episode |
| [`crystallization.md`](prompts/crystallization.md) | Synthesizes the last five episodes into a distilled checkpoint | Every 5 episodes |
| [`handoff.md`](prompts/handoff.md) | Generates the opening prompt for the next five-episode chat | Every 5 episodes, after crystallization |

### Characters

| File | What It Does |
|------|-------------|
| [`good-place-cast.md`](characters/good-place-cast.md) | Voice and personality guides for Eleanor, Chidi, Tahani, Jason, Michael, Janet, Bad Janet, and Michael Schur |
| [`generic-template.md`](characters/generic-template.md) | Blank template for defining any ensemble cast — fill in voice, worldview, blind spots, philosophical role |

### Templates

| File | What It Does |
|------|-------------|
| [`crystallization-template.md`](templates/crystallization-template.md) | Structure for your five-episode synthesis documents |
| [`arc-planning-template.md`](templates/arc-planning-template.md) | Structure for planning a full arc (theme, core question, episode sketches) |

### Vault Setup (Optional)

The [`vault-setup/`](vault-setup/) folder contains a guide for preserving your curriculum in an Obsidian knowledge vault. This is entirely optional — you don't need it to run the curriculum. It's there for anyone who wants a durable, searchable archive of their learning that survives platform changes. Think of it as a bonus for the more adventurous.

---

## Sample Episode Excerpt

Here's a brief look at what the conversation format actually feels like. This is a condensed, illustrative example — not a full episode transcript.

> **Topic:** What does "enough" mean?
> **Lead:** Eleanor, with Chidi

> **ELEANOR:** Okay, so here's my question. You've got this life — the job, the family, the hobbies, the whole deal. When you list it all out, it sounds like a lot. But my question isn't whether it's a lot. My question is: do you ever feel like you're doing all of it so you don't have to sit still?
>
> **You:** Honestly? I used to wonder that too. But I think there's a difference between filling time and being engaged. My schedule is full because I'm interested, not because I'm avoiding something.
>
> **ELEANOR:** See, that's a very reasonable answer. Chidi, back me up — that's exactly the kind of reasonable answer that makes me suspicious.
>
> **CHIDI:** I... actually think he might be right, Eleanor. There's a difference between Pascal's divertissement — distraction as escape — and genuine engagement. The question is whether the activity feels nourishing or numbing.
>
> **ELEANOR:** Fine. New question. When's the last time you did nothing and it felt good? Not productive nothing. Not meditation nothing. Just... nothing.
>
> **You:** Last Tuesday. My wife and I sat in the car after picking something up and just watched the ocean for ten minutes. No agenda. It was great.
>
> **ELEANOR:** *[long pause]* Okay. That's not the answer of someone who's running.

The full example with commentary is in [`examples/sample-episode-excerpt.md`](examples/sample-episode-excerpt.md).

---

## Adapting the Method

This method isn't limited to *The Good Place* or to philosophy. The core structure — ensemble characters, Socratic dialogue, crystallization checkpoints, character evolution — works for any domain where you want to explore questions through conversation.

Some possibilities:
- **Literature:** Characters from a novel or film exploring its themes through your experience (I did this with Walt Whitman's *Song of Myself* using real cultural figures as hosts)
- **History:** Historical figures examining contemporary questions through their particular lens
- **Career/Life:** Characters from a show you love helping you think through professional or personal crossroads
- **Creative work:** Characters serving as collaborators or critics for a creative project

Use the [`generic-template.md`](characters/generic-template.md) to define your cast. The key requirements: characters who think differently from each other, who would genuinely disagree, and who bring distinct perspectives to hard questions.

---

## Limitations and Honest Caveats

- **No peer review.** The philosophical content in my curriculum was not reviewed by academics. Where I had existing knowledge, the AI's treatment was nuanced and genuinely insightful. Where I didn't, I can't fully evaluate the accuracy. Bring your own critical thinking
- **AI over-affirms.** Even with instructions to push back, the AI tends to praise responses more than a human teacher would. Some characters (Eleanor, Bad Janet) naturally resist this; others need the nudge
- **Privacy is real.** AI conversations are not private in the way a therapist's office is. Your data is processed by the AI company. The likelihood of exposure is small, but the guarantee doesn't exist. Be as open as you're comfortable with
- **The AI can be wrong in ways you can't detect.** If you don't have background in the subject matter, you may not catch inaccuracies. This is personal exploration, not accredited education
- **Context window limits.** You can't run the whole curriculum in one chat. The five-episode segmentation with crystallization handoffs is the workaround, and it actually improves the experience

---

## Credits

This project wouldn't exist without *The Good Place* — created by Michael Schur, brought to life by a brilliant cast and writing team. The characters had enough philosophical depth that they could carry a stranger's education years after the show ended. That's extraordinary.

Built with [Claude](https://claude.ai) by Anthropic.

---

## License

This repo is shared under [MIT License](LICENSE). Use it, adapt it, make it yours. If you build something with it, I'd love to hear about it.
