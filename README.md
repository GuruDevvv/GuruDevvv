<a href="https://t.me/dshneyder"><img src="assets/header.jpg" width="100%" alt="Dmitry Shneyder. Twenty years turning chaos into systems: people, teams, businesses. Now building products with AI agents."></a>

<a href="https://t.me/dshneyder"><img src="https://img.shields.io/badge/Telegram-@dshneyder-111111?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram @dshneyder"></a>

I am a product person, not a developer. For twenty years my work has been people: psychology, training, teams. For the last year I have been building products with AI agents, and I do not write the code by hand. This account holds the part of that work anyone can pick up and use.

## my-claude-skills

<a href="https://github.com/GuruDevvv/my-claude-skills"><img src="assets/my-claude-skills.jpg" width="100%" alt="Claude Skills. Nine skills I wrote. Twelve I use."></a>

Nine skills I wrote for Claude Code and twelve third-party ones I use, kept in one place so the setup can be rebuilt on another machine.

**Why it exists.** When you do not write the code, what you control is how the work is set up before the agent starts: a spec, a check that the thing is worth building, a design picked from options, a review before any code exists. Each skill is one of those steps, written down once so I stop explaining it in every session.

**What it is.** Folders of instructions, some with scripts. Mine and third-party live in separate folders. The third-party ones are MIT, each with its author, source and licence text; two were broken on Windows and are patched, and each patch is described at the top of that skill's README.

<a href="https://github.com/GuruDevvv/my-claude-skills"><img src="https://img.shields.io/badge/Repository-FF4F1A?style=for-the-badge&logo=github&logoColor=white" alt="my-claude-skills on GitHub"></a>

Install: copy a skill's folder into `~/.claude/skills/<skill-name>/` and restart Claude Code.

## design-first

<a href="https://github.com/GuruDevvv/my-claude-skills/tree/main/mine/design-first"><img src="assets/design-first.jpg" width="100%" alt="Design First. Six first screens. Pick one. Get a live page."></a>

A Claude Code skill for people who are not designers: six different first screens for your topic, you pick one, and it is built as a live page for desktop and phone.

**Why it exists.** "Make it look good" is not a brief. Ask an agent for a page and you get the same clean modern layout every time. Choosing between six is easier than describing one.

**What it is.** One of the skills in the collection above. An image model draws six directions as mockups, three screens each, you pick one or mix two, the text is taken off the chosen mockup and the page is built with live text over it; the phone gets its own mockup. Before you see the page, a script opens it in a real browser at three widths and checks sideways scroll, unreadable text, missing fonts and broken images. It needs Node 22+, Chrome or Edge, and an image generator such as the Codex CLI.

<a href="https://github.com/GuruDevvv/my-claude-skills/tree/main/mine/design-first"><img src="https://img.shields.io/badge/Skill-FF4F1A?style=for-the-badge&logo=github&logoColor=white" alt="design-first skill on GitHub"></a>

Install: copy `mine/design-first/` from the collection into `~/.claude/skills/design-first/` and restart Claude Code.

## How the work is checked

Neither has an automated test suite of its own. What they have instead:

- **design-first** checks its own output. The page checker ships with control pages: four broken on purpose and two clean, with the expected verdict for each, so a green result means something. The switch to drawn mockups came out of seven blind rounds in September 2026: every screen I called a "wow" was drawn by an image model, none was written as HTML. The protocol is summarised inside the skill.
- **my-claude-skills** ships the research two of its skills came out of, next to the skill. One good third-party skill is left out on purpose: its repository has no licence file, so redistributing it would not be legal.

## Who writes the code

My part is the task, the decisions, and accepting or rejecting the result. The code and most of the text in this repository are written by AI agents: Claude Code does the work, and Codex is the second opinion and draws the pictures on this page.

The histories show it: as of 11 October 2026, 59 of the 67 public commits in my-claude-skills carry a `Co-Authored-By: Claude` trailer.
