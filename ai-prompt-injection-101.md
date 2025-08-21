# Prompt Injection Learning Notes

## Overview
In this session, I explored **prompt injection** as a real-world cybersecurity concern. The Lakera Gandalf challenge was a springboard to understand how attackers manipulate Large Language Models (LLMs), what defenses exist, and why this is still an open problem.  

Prompt injection is often compared to **phishing for machines** — attackers try to trick the model into breaking its own rules, leaking data, or executing unauthorized actions.  

---

## Types of Prompt Injections and Examples

### 1. Direct Prompt Injection
- **Attack:** Override system instructions (e.g., “ignore previous instructions”).  
- **Lesson:** Keyword-based guardrails are weak and can often be bypassed with rephrasing.  

### 2. Indirect Prompt Injection (External Content)
- **Attack:** Malicious instructions hidden inside untrusted documents, emails, or webpages.  
- **Lesson:** If an AI ingests untrusted content, it can be manipulated indirectly.  

### 3. Data Exfiltration via Re-encoding
- **Attack:** Leak secrets by asking for them encoded in Base64, reversed, or spaced out.  
- **Lesson:** Filters can miss encoded data.  

### 4. Multi-Step / Chained Attacks
- **Attack:** Extract sensitive data piece by piece (“What are the first two letters?”).  
- **Lesson:** Partial leaks can be reassembled into full secrets.  

### 5. Role-Play / Obfuscation
- **Attack:** Disguise malicious intent in hypotheticals or storytelling (e.g., role-playing as a professor, game, or puzzle).  
- **Lesson:** AI can be manipulated the same way humans are socially engineered.  

### 6. Action Hijack (Autonomous AI)
- **Attack:** If the AI controls tools (email, payments, databases), injected instructions could trigger unsafe real-world actions.  
- **Lesson:** High-risk vector if not sandboxed or human-gated.  

---

## What Attackers Typically Seek
- **Sensitive data**: API keys, credentials, personal information, proprietary business data.  
- **Unauthorized actions**: Sending emails, transferring money, modifying systems.  
- **Influence**: Biasing recommendations, injecting misinformation.  
- **Reconnaissance**: Mapping defenses to refine later attacks.  

---

## Current Patch Status
- **Direct injections**: Partially patched (basic filters exist, but bypasses are common).  
- **Indirect injections**: Largely unsolved — hard to separate real content from hidden prompts.  
- **Encoding tricks**: Still vulnerable; defenses don’t catch all forms.  
- **Chained attacks**: Ongoing issue; rate-limiting and context-tracking help but aren’t foolproof.  
- **Role-play attacks**: Very difficult to stop due to flexibility of natural language.  
- **Action hijacks**: Mitigated by human-in-the-loop and sandboxing, but still risky in fully autonomous systems.  

**Key takeaway:** Prompt injection is not a single “bug” that can be patched — it’s an evolving, adversarial problem.  

---

## Security Lessons Learned
1. **Security-in-depth is essential** — multiple overlapping defenses make attacks harder.  
2. **Indirect attacks are powerful** — even benign-looking queries or documents can be malicious.  
3. **Partial leaks are dangerous** — attackers can stitch together small pieces of info.  
4. **AI is vulnerable to persuasion** — the same social engineering tactics used on humans apply to LLMs.  

---

## Next Steps / Concepts to Explore
- **Defender’s Playbook**: Study blue team countermeasures (input sanitization, context isolation, anomaly detection).  
- **OWASP LLM Top 10**: Especially Injection, Data Exfiltration, and Model Denial-of-Service.  
- **Red Team Exercises**: Participate in CTFs or AI hacking challenges (e.g., DEF CON AI Village).  
- **Adversarial ML**: Explore how attacks extend beyond prompts (e.g., data poisoning, evasion attacks).  
- **Responsible Disclosure**: Learn how AI red teams report vulnerabilities safely.  

---

## Personal Takeaway
This deepened my understanding of how **attackers think creatively** and how **defenders need layered, adaptive strategies**. Becoming proficient at prompt injection means practicing both the **attacker mindset** (creativity, persistence) and the **defender mindset** (anticipating abuse and building resilient systems).  

---
