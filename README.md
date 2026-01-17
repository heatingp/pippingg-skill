# pippingg-skill

Claude Code skills for deep thinking and content creation.

[中文版](README.zh.md)

## Installation

**Method 1: Add Marketplace (Recommended)**
```
/plugin marketplace add heatingp/pippingg-skill
```

**Method 2: Direct Install**
```
/plugin install thinking-skills@pippingg-skill
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

## Why These Skills?

**The Problem:** AI assistants tend to be "yes-men" — they agree with everything, give surface-level analysis, and stay within your mental framework.

**The Solution:** These skills train Claude to be a true thinking partner:
- Challenge your ideas (but ask about context first)
- Use Socratic questioning instead of lecturing
- Help you discover insights yourself
- Continuously improve through conversation feedback

## License

MIT
