# pippingg-skills

Claude Code skills for deep thinking, content creation, and recipe generation.

[中文版](README.zh.md)

## Installation

**Method 1: Add Marketplace (Recommended)**
```
/plugin marketplace add heatingp/pippingg-skills
```

**Method 2: Direct Install**
```
/plugin install thinking-skills@pippingg-skills
/plugin install content-skills@pippingg-skills
```

## Available Skills

### 1. socratic-thinking

A Socratic questioning partner that helps you think deeply and write articles.

**What it does:**
- Challenges your assumptions using first-principles thinking
- Distinguishes real problems from emotional reactions
- Helps you break out of mental frameworks
- Guides you from scattered thoughts to structured articles

**Key features:**
- **Boundary checking**: Asks about context before challenging your ideas (avoids nitpicking)
- **First-principles analysis**: Gets to the root of problems instead of surface-level discussion
- **Reverse thinking**: "What if the opposite were true?"
- **Penetrating questions**: Follows the money, identifies beneficiaries, reveals hidden interests
- **Scaffolding**: When you're stuck, provides smaller stepping stones instead of answers

**Anti-patterns it avoids:**
- Being a "yes-man" that agrees with everything
- Giving 400-word lectures instead of asking questions
- Challenging conclusions without understanding premises
- Staying within your mental framework instead of helping you escape it

**Usage:**
```
/socratic-thinking
```
Or simply say: "help me think", "I want to discuss", "let's analyze this"

---

### 2. skill-iterator

Automatically iterates and updates skills based on conversation feedback.

**What it does:**
- Extracts feedback from your conversation with AI
- Tracks the feedback → correction → confirmation loop
- Generates diff previews before applying changes
- Maintains a CHANGELOG for skill evolution

**Commands:**
```
/skill-iterator              # Update the skill used in current conversation
/skill-iterator <skill-name> # Update a specific skill
/feedback <content>          # Explicitly mark important feedback (higher priority)
```

**How it works:**
1. Identifies the target skill
2. Reads SKILL.md and CHANGELOG.md
3. Analyzes conversation history for feedback loops
4. Generates suggested changes with diff preview
5. Applies changes after your confirmation

**Smart suggestions:**
- Detects sections modified 3+ times → suggests adding dedicated section
- Detects flip-flop changes → warns before reverting
- Detects recurring feedback patterns → suggests restructuring

**Usage:**
After using any skill and providing feedback during the conversation:
```
/skill-iterator
```

---

### 3. recipe-generator

Generates professional-grade recipes with detailed instructions and image prompts.

**What it does:**

- Searches authoritative sources (Michelin Guide, 舌尖上的中国, professional chefs)
- Generates precise recipes with exact measurements and timing
- Creates image prompts for recipe posters in multiple styles
- Automatically generates recipe poster images using Gemini

**Key features:**

- **Authoritative sources**: Pulls from Michelin, 舌尖上的中国, top-rated recipes
- **Precise measurements**: No vague "to taste" — exact grams and milliliters
- **Professional tips**: Chef techniques that make a real difference
- **Image generation**: Creates beautiful recipe posters automatically

**Style options:**

| Style | Description |
| ----- | ----------- |
| C (default) | Modern realistic, educational |
| A | Traditional poster, high visual impact |
| B | Literati scroll, elegant and refined |

**Usage:**

```
/recipe-generator 清蒸鱼
/recipe-generator 红烧肉 plan A风格
```

**Dependencies:**

- Thanks to [cclank/recipe-generator](https://github.com/cclank/recipe-generator/) for the inspiration and foundational work

- `baoyu-gemini-web` — for generating recipe poster images

## Why These Skills?

**The Problem:** AI assistants tend to be "yes-men" — they agree with everything, give surface-level analysis, and stay within your mental framework.

**The Solution:** These skills train Claude to be a true thinking partner:
- Challenge your ideas (but ask about context first)
- Use Socratic questioning instead of lecturing
- Help you discover insights yourself
- Continuously improve through conversation feedback

## License

MIT
