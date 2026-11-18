# first-time-right

**A Claude Code skill: choose the path by the result the person will accept on the first try.**

An agent usually starts with whatever is already open: the file in front of it, the first search hit, the blurry screenshot it was handed. The work looks finished, and the person sends it back. Then they suggest the path themselves, which is the work the agent was meant to do.

**The person's time is the scarcest resource in the system.** The agent does the thinking, the searching and the checking. The person gives decisions and approvals.

## What it does

**Before the first action**, the agent writes one line: the result the person will accept, and how it will be checked. Then it looks for the best source for that result, not only the nearest one, and compares at least two when the source decides the quality.

**It lists what the path would leave to the person** (doing, hinting, finding, checking) and takes each item back. Only decisions and approvals stay with the person.

**It switches path before working**, without asking, when the signals show up: the source was picked because it was open; the material is small, partial or blurry; a third attempt on the same material is needed; the person's words describe a result and were read as a method.

**When it delegates**, the brief carries the result, the acceptance check and the source, ready to use. Choosing the source is not passed down.

**Before handing over**, it opens the result and compares it with the line it wrote at the start. If they don't match, it redoes the work in the same turn.

**When the person had to suggest the path**, the agent does it their way at once and records what was missed. A miss that happens twice becomes a rule the agent reads before every answer, in a hook or a system prompt, so nobody has to remember to look it up.

Choosing the method never grants the right to publish, send, spend or change the agreed scope.

## Install

```bash
git clone https://github.com/estherwow/first-time-right.git ~/.claude/skills/first-time-right
```

## Origin

Written from practice: a business run on two AI agents. Every time the person had to point to a better source or ask for a redo, the case went into a log. This skill is what those cases had in common. Before publishing, a second agent (Codex) read it without any context about the project and checked it against its own work.

Related: [constraint-first](https://github.com/estherwow/constraint-first) (close the constraints before generating) · [shared-journal](https://github.com/estherwow/shared-journal) (one memory for several chats).

MIT
