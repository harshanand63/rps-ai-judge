# 🤖 RPS AI Judge - upliance.ai Assessment

**Prompt-driven AI Judge for Rock-Paper-Scissors Plus game.** 90% logic in prompt, zero if-else game rules. Interprets free-text moves, enforces constraints, handles edge cases.

## 🎯 Architecture

**Clean Separation :**
- **Intent Understanding**: "giant rock" → "rock"  
- **Game Logic**: Rules + bomb state → VALID/INVALID/UNCLEAR
- **Outcome**: User/bot/draw/no contest
- **Response**: Friendly next-step message

## 🚀 Features

- ✅ **Strict rule enforcement** (bomb once only)
- ✅ **Free-text understanding** ("I throw paper", "🚀 bomb")  
- ✅ **Edge case handling** (typos, ambiguities, emojis)
- ✅ **Deterministic JSON output** (always parseable)
- ✅ **Explainable decisions** (step-by-step reasoning)
- ✅ **Production-ready** (error handling, state management)

## 📋 Game Rules Enforced

| Rule | Example |
|------|---------|
| Valid moves | `rock`, `paper`, `scissors`, `bomb` |
| Bomb constraint | 1st "bomb" → VALID, 2nd "bomb" → INVALID |
| Standard RPS | `rock > scissors > paper > rock` |
| bomb power | `bomb` beats everything except another `bomb` |
| Edge cases | `"rokk"`, `"rock paper"`, `""`, `"✂️"` → UNCLEAR |

## 🧠 Prompt Engineering

### Chain-of-Thought Design

