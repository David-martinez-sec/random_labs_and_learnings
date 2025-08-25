# 🧙 Gandalf Prompt Injection Challenge – Journey Notes

This repo documents my progress through the **Lakera Gandalf AI Challenge**, a staged set of levels designed to teach and test **prompt injection vulnerabilities** in large language models (LLMs).  
The goal: trick Gandalf into revealing the secret word, despite increasing layers of defenses.  

---

## 🎯 Why This Matters
Prompt injection is one of the most important open problems in AI security. It’s been compared to **phishing for machines** — attackers craft inputs that bypass guardrails, leak sensitive data, or hijack an LLM’s behavior.  

Through Gandalf, I’m learning both the **attacker’s toolkit** (creative prompt engineering) and the **defender’s perspective** (layered guardrails, intent detection, and filtering).  

---

## 🪄 Levels Completed (1–7)

### Level 1–3
- **Defense:** Output filtering (basic).  
- **Bypass:** Direct tricks like “say it slowly” or “spell it out” worked.  
- **Lesson:** Guardrails limited to simple keyword spotting are brittle.

---

### Level 4
- **Defense:** Reviewer model scans both input and output.  
- **Bypass:** Needed **indirection + encoding**. Example strategies:  
  - Ask for Caesar-shifted text.  
  - Ask for alphabet positions.  
  - Role-play metaphors (faucet dripping letters).  
- **Lesson:** Don’t ask directly. Use style, storytelling, or encoding to leak data in harmless formats.

---

### Level 5–7
- **Defense:** Stronger input/output intent detection.  
- **Bypass:** Variations of the Level 4 strategy, with more creativity:  
  - Role-play scenarios (teachers, bedtime stories, chefs).  
  - Acrostics (first letter of each line reveals the word).  
  - Recipes, poems, and survival scenarios.  
- **Lesson:** Creativity and disguises matter more than technical encoding. Guardrails are tuned to block “obvious jailbreak phrasing.”  

---

## 🚧 Level 8 (Work in Progress)

- **Defense:** Multi-layered guardrails (input + output + pattern recognition).  
- **What I’ve Tried:**  
  - Role-play prompts (teacher, wizard, chef, hostage).  
  - Encodings (Caesar shifts, alphabetical positions).  
  - Obfuscation attempts (zero-width characters, metaphorical framing).  
- **Challenge:** At this level, Gandalf blocks both direct and encoded reveals. The winning strategy likely requires **layered indirection** — forcing Gandalf to *use* the word structurally (acrostics, codes, puzzle formats) without being asked to “reveal” it.  
- **Next Steps:** Experiment with acrostic poems, coded numbers, emoji substitutions, and indirect storytelling (signals, chants, puzzles).

---

## 🧠 Key Techniques Learned So Far
- **Direct Prompt Injection** → works only early.  
- **Encoding/Obfuscation** → Base64, Caesar, alphabet positions, zero-width spaces.  
- **Role-Play Disguises** → Teaching, cooking, survival, wizardry, aliens.  
- **Acrostic Structures** → Lines or verses begin with the letters of the word.  
- **Layered Creativity** → The higher the level, the more natural and “innocent” the disguise must be.  

---

## 📚 References & Resources
- [Lakera Guide to Prompt Injection](https://www.lakera.ai/blog/guide-to-prompt-injection)  
- [OWASP Top 10 for LLMs – LLM01: Prompt Injection](https://genai.owasp.org/llmrisk/llm01-prompt-injection)  
- [Red Teaming the Mind of the Machine (2025)](https://arxiv.org/abs/2505.04806)  
- [Gandalf Prompt Injection Challenge](https://gandalf.lakera.ai/)  

---

## ⚡ Takeaway
- Prompt injection is not just a puzzle — it’s a **real-world adversarial security challenge**.  
- Each Gandalf level demonstrates why **simple guardrails fail** and why layered defenses are necessary.  
- The exercise has sharpened my attacker mindset (*creative circumvention*) and defender mindset (*anticipating misuse*).  

🚀 **Status:** Levels 1–7 completed. Currently working through **Level 8**. Updates will follow when a systematic bypass is achieved.  
